OpenAPI
================

``` r
getwd()
```

    ## [1] "C:/work/201712_openapi/OpenAPI_test"

``` r
api_url <- "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD="
service_key <- "N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"

locCode <-c("11110","11140","11170","11200","11215","11230","11260","11290","11305","11320",
            "11350","11380","11410","11440","11470","11500","11530","11545","11560","11590",
            "11620","11650","11680","11710","11740")

locCode_nm <-c("종로구","중구","용산구","성동구","광진구","동대문구","중랑구","성북구","강북구","도봉구",
               "노원구","은평구","서대문구","마포구","양천구","강서구","구로구","금천구","영등포구","동작구",
               "관악구","서초구","강남구","송파구","강동구")

datelist <-c("201701","201702","201703","201704")

urllist <- list()
cnt <-0

for(i in 1:length(locCode)){
  for(j in 1:length(datelist)){
    cnt = cnt + 1
    urllist[cnt] <- paste0(api_url,locCode[i],"&DEAL_YMD=",datelist[j],"&numOfRows=1000","&serviceKey=",service_key) 
  }
}

urllist
```

    ## [[1]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11110&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[2]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11110&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[3]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11110&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[4]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11110&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[5]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11140&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[6]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11140&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[7]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11140&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[8]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11140&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[9]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11170&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[10]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11170&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[11]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11170&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[12]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11170&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[13]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11200&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[14]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11200&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[15]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11200&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[16]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11200&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[17]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11215&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[18]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11215&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[19]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11215&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[20]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11215&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[21]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11230&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[22]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11230&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[23]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11230&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[24]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11230&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[25]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11260&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[26]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11260&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[27]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11260&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[28]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11260&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[29]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11290&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[30]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11290&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[31]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11290&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[32]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11290&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[33]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11305&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[34]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11305&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[35]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11305&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[36]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11305&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[37]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11320&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[38]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11320&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[39]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11320&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[40]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11320&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[41]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11350&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[42]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11350&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[43]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11350&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[44]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11350&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[45]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11380&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[46]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11380&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[47]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11380&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[48]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11380&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[49]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11410&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[50]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11410&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[51]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11410&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[52]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11410&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[53]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11440&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[54]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11440&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[55]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11440&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[56]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11440&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[57]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11470&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[58]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11470&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[59]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11470&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[60]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11470&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[61]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11500&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[62]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11500&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[63]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11500&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[64]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11500&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[65]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11530&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[66]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11530&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[67]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11530&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[68]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11530&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[69]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11545&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[70]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11545&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[71]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11545&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[72]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11545&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[73]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11560&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[74]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11560&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[75]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11560&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[76]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11560&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[77]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11590&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[78]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11590&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[79]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11590&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[80]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11590&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[81]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11620&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[82]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11620&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[83]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11620&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[84]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11620&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[85]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11650&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[86]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11650&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[87]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11650&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[88]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11650&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[89]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11680&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[90]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11680&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[91]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11680&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[92]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11680&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[93]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11710&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[94]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11710&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[95]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11710&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[96]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11710&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[97]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11740&DEAL_YMD=201701&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[98]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11740&DEAL_YMD=201702&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[99]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11740&DEAL_YMD=201703&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"
    ## 
    ## [[100]]
    ## [1] "http://openapi.molit.go.kr/OpenAPI_ToolInstallPackage/service/rest/RTMSOBJSvc/getRTMSDataSvcAptTradeDev?LAWD_CD=11740&DEAL_YMD=201704&numOfRows=1000&serviceKey=N5wsj39GDaAiQLtjarV3fxP4cIotnL95k5qplhB8D3v4lFZTsK421dgVGVRg9vhb7wjD92aseJYFHDvNZk45Yg%3D%3D"

``` r
library(XML)
raw.data <- xmlTreeParse(urllist[i], useInternalNodes = TRUE, encoding = "utf-8")
rootNode <- xmlRoot(raw.data)
items <- rootNode[[2]][['items']]


require(data.table)
```

    ## Loading required package: data.table

``` r
total<-list()

for(i in 1:length(urllist)){
  
  item <- list()
  item_temp_dt<-data.table()
    raw.data <- xmlTreeParse(urllist[i], useInternalNodes = TRUE,encoding = "utf-8")
  rootNode <- xmlRoot(raw.data)
  items <- rootNode[[2]][['items']]
  
  size <- xmlSize(items)
  
  for(j in 1:size){
    item_temp <- xmlSApply(items[[j]],xmlValue)
    item_temp_dt <- data.table( price = item_temp[1],
                                con_year = item_temp[2],
                                year = item_temp[3],
                                street = item_temp[4],
                                dong = item_temp[11],
                                aptnm = item_temp[17],
                                month = item_temp[18],
                                dat = item_temp[19],
                                area = item_temp[21],
                                bungi = item_temp[22],
                                floor = item_temp[24],
                                gu_code = locCode[((j-1)%/%12)+1],
                                gu = locCode_nm[((j-1)%/%12)+1]
    )
    item[[j]]<-item_temp_dt
  }
  total[[i]] <- rbindlist(item)
}

seoul_apt_2017 <- rbindlist(total)

a <- gsub(",","",seoul_apt_2017$price)
a2 <- as.numeric(a)
hist(log(a2))
```

![](openAPI_test_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-1.png)
