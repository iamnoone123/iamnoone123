export Y = 2000
export M = 12
export D = 20
export GIT_COMMITTER_DATE="$Y-$M-$D 12:00:00"   
export GIT_AUTHOR_DATE="$Y-$M-$D 12:00:00"   
git commit --date="$Y-$M-$D 12:00:00" -m "Committed on $M $D $Y"

for VAR_NAME in {start..end}

for Y in {1999..2018}
    for M in {01..12}
        for D in {01..28}
        
        echo "Committed on $M/$D/$Y" > commit.md

for Y in {1999..2018}
do
  mkdir $Y
  for M in {01..12}
  do
    cd $Y
    mkdir $M
    cd ../
    for D in {01..28}
    do
      cd $Y/$M
      mkdir $D
      cd $D
      echo "Committed on $M/$D/$Y" > commit.md
      cd ../../../
      export GIT_COMMITTER_DATE="$Y-$M-$D 12:00:00"
      export GIT_AUTHOR_DATE="$Y-$M-$D 12:00:00"
      git add $Y/$M/$D/commit.md -f
      git commit --date="$Y-$M-$D 12:00:00" -m "$M $D $Y"
      git push origin master
    done
  done
done

for Y in {1999..2018}
do
  mkdir $Y
  cd $Y
  ...
        git add commit.md -f
        git commit --date="$Y-$M-$D 12:$i:00" -m "$i on $M $D $Y"
      done
      cd ../
    done
    cd ../
  done
  cd ../
done
git push origin master
