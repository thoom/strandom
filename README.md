# Thoom::Strandom
Random string command line script

## Installation

    gem install strandom

## CLI HELP 

    Usage: strandom [options]

    Specific options:
	        --alnum  [length]            Characters a-z, A-Z, 0-9
	        --alpha  [length]            Characters a-z, A-Z
	        --custom values,[length],[delimiter]
	                                     Provide a custom set of values to build the string
	        --lower  [length]            Characters a-z
	        --lownum [length]            Characters a-z, 0-9
	        --hex    [length]            Characters a-f, 0-9
	        --num    [length]            Characters 0-9
	        --uuid                       UUID v4 string
	        --upper  [length]            Characters A-Z
	        --upnum  [length]            Characters A-Z, 0-9
	
    Common options:
	        --help                       Shows this message
	        --version                    Current version

### Examples
#### Basic

    $ strandom --lownum 10
    => eh8zuzk71s 

#### UUID

    $ strandom --uuid
    => 89657eaf-4e07-43a7-b3de-b7d1f3c26940

#### Custom

    strandom --custom [String of values to randomize],[length of string],[String delimiter, defaults to single character]

Examples:

    $ strandom --custom "%4*?",10 
    => *%44*?%4**
	
    $ strandom --custom "%|4|*|,|?",10,"|"
    => ??4,%%,*%4
