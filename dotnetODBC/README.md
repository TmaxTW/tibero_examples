# Sample Code for dotnet ODBC in C#
## Building and running procedures
    #dotnet new console
    #dotnet add package System.Data.Odbc
    . ./setenv.sh
    dotnet build
    dotnet run

# Required environment variables:  
## Enable Unicode Support - Required before running "dotnet run" and "iuodbc/iusql"
    export TB_NLS_LANG=UTF8  
    export TBCLI_WCHAR_TYPE=UCS2  

# Optional environment variables:  
## Set odbc.ini and tbdsn.tbr location
    export TB_DSN_FILE=`pwd`/tbdsn.tbr  
    export ODBCINI=`pwd`/odbc.ini  

## Enable Trace - Useful when testing connection with isql and iusql
    export TBCLI_LOG_LVL=trace  
    export TBCLI_LOG_DIR=`pwd`  
