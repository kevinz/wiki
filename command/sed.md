#递归替换Always为IfNotPresent
find . -name "*.yaml" | xargs sed -i -e "s%Always%IfNotPresent%g"
