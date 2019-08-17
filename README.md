# ShorteningURL
Shortening Service

1. 프로젝트 소개
 해당 프로젝트는 URL을 입력받아 내부적으로 알고리즘을 통하여 입력받은 URL을 단축URL로 변경시켜주는 프로젝트입니다.
 개발은 JAVA, JSP를 사용하여 MVC2 패턴으로 개발하였고, 추가적으로 사용한 프레임웨크는 Bootstrap입니다.
 DataBase는 SQLITE를 사용하였습니다.

2. 문제해결 전략  
  1.) 처음 번경전URL을 입력하게되면 DB에 있는 URL값인지 아닌지 판별후 있으면 DB에 있는 단축URL(URL_SHORT) 결과를 리턴해주고 
   없는경우는 DB에 INSERT 시켜줍니다.    
  2.) DB TABLE의 컬럼은 IDX(LONG), URL_ORIGINAL(NVARCHAR), URL_SHORT(NVARCHAR)로 구성하였습니다.  
  3.) DB에 INSERT해줄때 IDX는 0부터 1씩 증가하여 넣어주고 이떄 변경할 URL주소를 URL_ORIGINAL 컬럼에 동시에 넣어줍니다.  
  4.) URL_SHORT의 값은 IDX를 [a~z],[A~Z],[0~9]를 통하여 62진수로 Encoding 하여 넣어줍니다.
 
 
3. 프로젝트 빌드, 실행방법
 1.)새로운 workspace생성 
 2.)폴더안에 있는 KwonSoonKyu 파일과 KwonSoonKyu_Server 파일을 각각 이클립스에서 Import 시켜줍니다.  
    (General -> Existing Projects into Workspace -> select archive file -> KwonSoonKyu, KwonSoonKyu_Server 선택 후 Finish)    
 3.)폴터안에 있는 Tomcat 파일을 C:\Tomcat 경로로 이동시켜줍니다. 
 4.)폴더안에 있는 KwonSql 파일을 C:\ 경로로 이동시켜줍니다. 
 5.)WebContent -> Main -> Shortening_Url.jsp를 실행합니다.



