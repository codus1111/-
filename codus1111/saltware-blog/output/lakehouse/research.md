# 리서치: 레이크하우스
조사일: 2026-11-02

## 핵심 사실
1. 데이터 웨어하우스는 정리된 정형 데이터를 BI(보고서·대시보드)용으로 제공한다. 데이터 레이크는 어떤 형식의 데이터든 싸게 보관한다. (출처: https://docs.databricks.com/lakehouse)
2. 데이터 레이크는 오디오, 영상, JSON 등 모든 형식을 담을 수 있는 저비용 개방형 저장소다. (출처: https://www.databricks.com/it/blog/2021/08/30/frequently-asked-questions-about-the-data-lakehouse.html)
3. 레이크하우스는 레이크와 웨어하우스의 장점을 합친 데이터 관리 시스템이다. (출처: https://docs.azure.cn/en-us/databricks/lakehouse/)
4. 레이크하우스는 개방형 데이터 레이크 위에 데이터 관리·성능 기능을 더해 BI와 머신러닝을 함께 지원한다. (출처: 2번과 같은 Databricks FAQ)
5. Databricks 레이크하우스의 핵심 기술은 저장 계층 Delta Lake와 데이터·AI 거버넌스 계층 Unity Catalog다. (출처: https://docs.databricks.com/lakehouse)
6. 데이터 늪(data swamp)은 거버넌스, 메타데이터, 품질 관리가 데이터 유입 속도를 못 따라가서 쓸모를 잃은 데이터 레이크를 말한다. 형식 불일치, 중복, 깨진 메타데이터가 생긴다. (출처: https://atlan.com/data-lake-vs-data-swamp/ , https://www.cdata.com/blog/data-swamp)
7. 거버넌스, 품질 절차, 데이터 정리를 도입하면 늪에서 레이크나 레이크하우스로 되돌릴 수 있다. (출처: https://www.cdata.com/blog/data-swamp)
8. Starburst는 Trino 기반으로, 데이터를 옮기거나 복사하지 않고 있는 자리에서 조회한다. 커넥터가 50개 이상이다. 다만 네트워크 지연이 생길 수 있다는 지적도 있다. (출처: https://www.starburst.io/resources/starburst-brochure , https://www.modern-datatools.com/compare/databricks-vs-starburst)

## 비유·예시 소재
- 웨어하우스 = 선반과 라벨이 정해진 창고
- 레이크 = 뭐든 부어 넣는 호수. 관리 안 하면 늪
- 레이크하우스 = 호숫가에 지은 집(호수의 넉넉함 + 집의 정리)
- 예: 매출 표(정형) + 상담 녹음·계약서 PDF(비정형)를 한곳에서 같이 보기

## 솔트웨어 연결 지점
- 데이터 사업: Databricks, Starburst, Sapie-Lake (style-guide.md 기본 정보)
- 전부 옮기기 부담스러운 고객에게는 Starburst로 제자리 조회부터 시작하는 선택지

## 참고 링크
- Databricks 공식 문서, What is a data lakehouse: https://docs.databricks.com/lakehouse
- Databricks 블로그, Lakehouse FAQ: https://www.databricks.com/it/blog/2021/08/30/frequently-asked-questions-about-the-data-lakehouse.html
- Azure Databricks 문서: https://docs.azure.cn/en-us/databricks/lakehouse/
- Atlan, Data Lake vs Data Swamp: https://atlan.com/data-lake-vs-data-swamp/
- CData, What is a Data Swamp: https://www.cdata.com/blog/data-swamp
- Starburst 브로슈어: https://www.starburst.io/resources/starburst-brochure
