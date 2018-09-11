# bash-aliases
```bash
alias clint="cpplint --recursive --filter=-legal/copyright,-whitespace/comments,-whitespace/end_of_line,-whitespace/indent,-whitespace/ending_newline"

alias subl="/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl"

function cfmt {
	if [ -z "$1" ]
	then
		return 1
	fi
	files=$(find $1 -iname '*.h' -o -iname '*.cpp' -o -iname '*.hpp' -o -iname '*.inl' -o -iname '*.c' -o -iname '*.cxx')
	for i in $files; do
		echo $i;
    	clang-format -i $i;
	done
}
```
