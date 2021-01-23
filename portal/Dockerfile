FROM liferay/portal:7.3.5-ga6

COPY tomcat/setenv.sh /opt/liferay/tomcat/bin/setenv.sh
COPY configs/portal-ext.properties /opt/liferay/portal-ext.properties
COPY configs/com.liferay.portal.search.elasticsearch7.configuration.ElasticsearchConfiguration.config /opt/liferay/osgi/configs/com.liferay.portal.search.elasticsearch7.configuration.ElasticsearchConfiguration.config