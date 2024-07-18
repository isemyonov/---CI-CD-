Тема проектной работы: Обеспечение безопасной работы веб-приложения с использованием, Виртуализации, Мониторинга, Резервного копирования и CI/CD инструментов» принята на рассмотрение 

Проект направлен на обеспечение безопасной работы веб-приложения с использованием различных технологий, включая виртуализацию, мониторинг, резервное копирование и CI/CD инструменты. Вот описание целевой архитектуры:

Пользователь:
Взаимодействует с веб-приложением через интернет.

Брандмауэр:
Обеспечивает первичный уровень безопасности, фильтруя входящий и исходящий трафик, защищая внутреннюю сеть от несанкционированного доступа.

Балансировщик нагрузки:
Распределяет входящий трафик между несколькими серверами веб-приложения для обеспечения отказоустойчивости.

Веб-серверы:
Виртуальные машины (VM), на которых размещено само веб-приложение. Виртуализация позволяет гибко управлять ресурсами и улучшать изоляцию приложений.

Сервер базы данных:
Виртуальная машина, на котором хранится база данных веб-приложения. Виртуализация позволяет легко масштабировать и управлять базой данных.

Мониторинг:
Система мониторинга  Prometheus, Grafana, AlertManger отслеживает состояние серверов, базы данных и сетевых компонентов, собирает метрики и отправляет оповещения в случае сбоев или аномалий.

Резервное копирование:
Механизм автоматического создания резервных копий данных и конфигураций, что позволяет восстановить работу приложения в случае сбоя или потери данных. Это может быть реализовано с использованием таких инструментов, как BorgBackup.

CI/CD (Continuous Integration/Continuous Deployment):
Инструменты для автоматизации процессов сборки, тестирования и деплоя приложения (например, Jenkins, GitLab CI/CD). Они обеспечивают быстрое и безопасное развертывание обновлений приложения.

Система управления конфигурацией:
Используется для автоматизации управления и развертывания инфраструктуры (например, Ansible, Puppet, Chef). Это позволяет централизованно управлять настройками всех компонентов системы.

Как это работает вместе:

Безопасность и управление доступом:

Брандмауэр защищает систему от внешних угроз.
Балансировщик нагрузки распределяет трафик, улучшая отказоустойчивость.
Мониторинг обеспечивает постоянное наблюдение за состоянием системы, позволяя быстро реагировать на проблемы.
Система резервного копирования защищает данные и позволяет быстро восстановить систему в случае сбоев.
Автоматизация и управление инфраструктурой:

Виртуализация позволяет гибко управлять ресурсами и изоляцией приложений.
CI/CD инструменты автоматизируют процесс развертывания и тестирования, обеспечивая быструю и безопасную доставку обновлений.
Система управления конфигурацией автоматизирует развертывание и настройку инфраструктуры, снижая вероятность ошибок и улучшая управляемость.
Эта архитектура позволяет создать надежное и безопасное веб-приложение, которое легко масштабировать, мониторить и поддерживать.
 
[Uploading Диаграмма без названия.drawio…]()<mxfile host="app.diagrams.net" modified="2024-07-18T22:08:52.285Z" agent="Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/126.0.0.0 Safari/537.36" etag="ijIGR9hJDafOIaZtwVLe" version="24.7.1" type="device">
  <diagram id="6a731a19-8d31-9384-78a2-239565b7b9f0" name="Page-1">
    <mxGraphModel dx="552" dy="287" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="827" pageHeight="1169" background="none" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2288" value="" style="rounded=1;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="242.5" y="298" width="461" height="810" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2285" value="" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=#BAC8D3;fontSize=24;fontColor=#23445D;align=center;opacity=60;" vertex="1" parent="1">
          <mxGeometry x="283" y="358" width="380" height="164" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2286" value="" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=#BAC8D3;fontSize=24;fontColor=#23445D;align=center;opacity=60;verticalAlign=middle;" vertex="1" parent="1">
          <mxGeometry x="278.5" y="838.5" width="380" height="240" as="geometry" />
        </mxCell>
        <mxCell id="2093" value="" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=#BAC8D3;fontSize=24;fontColor=#23445D;align=center;opacity=60;" parent="1" vertex="1">
          <mxGeometry x="283" y="558" width="380" height="240" as="geometry" />
        </mxCell>
        <mxCell id="2103" value="Nginx" style="shape=mxgraph.cisco.servers.fileserver;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=14;fontColor=#000000;" parent="1" vertex="1">
          <mxGeometry x="447" y="388" width="43" height="62" as="geometry" />
        </mxCell>
        <mxCell id="2109" value="ISP 1" style="shape=mxgraph.cisco.storage.cloud;html=1;dashed=0;strokeColor=#23445D;fillColor=#ffffff;strokeWidth=2;fontFamily=Helvetica;fontSize=24;fontColor=#23445D;align=center;fontStyle=1" parent="1" vertex="1">
          <mxGeometry x="503" y="16" width="186" height="106" as="geometry" />
        </mxCell>
        <mxCell id="2110" value="ISP 2" style="shape=mxgraph.cisco.storage.cloud;html=1;dashed=0;strokeColor=#23445D;fillColor=#ffffff;strokeWidth=2;fontFamily=Helvetica;fontSize=24;fontColor=#23445D;fontStyle=1" parent="1" vertex="1">
          <mxGeometry x="961" y="16" width="186" height="106" as="geometry" />
        </mxCell>
        <mxCell id="2138" value="" style="shape=mxgraph.cisco.routers.router;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=36;fontColor=#FFB366" parent="1" vertex="1">
          <mxGeometry x="790" y="154" width="78" height="53" as="geometry" />
        </mxCell>
        <mxCell id="2175" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4" parent="1" source="2110" target="2109" edge="1">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2259" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;exitX=0.474;exitY=0.363;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1" source="2138">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="822" y="280" as="sourcePoint" />
            <mxPoint x="827" y="70" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2260" value="&lt;font color=&quot;#23445d&quot;&gt;Jira cluster&amp;nbsp;&lt;/font&gt;" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=none;fontSize=14;fontColor=#742B21;align=center;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="519.5" y="568" width="139" height="19" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2262" value="&lt;div style=&quot;line-height: 0%;&quot;&gt;&lt;span style=&quot;font-size: 14px; background-color: initial;&quot;&gt;&lt;font color=&quot;#000000&quot;&gt;jira [nod_1]&lt;/font&gt;&lt;/span&gt;&lt;br&gt;&lt;/div&gt;" style="shape=mxgraph.cisco.servers.fileserver;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=36;fontColor=#FFB366" vertex="1" parent="1">
          <mxGeometry x="329" y="613.5" width="43" height="62" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2269" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;entryX=1;entryY=0.5;entryDx=0;entryDy=0;entryPerimeter=0;exitX=0;exitY=0.5;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1" target="Xr0FSyJAFfYrDeTETw8K-2262">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="569" y="644.5" as="sourcePoint" />
            <mxPoint x="337" y="772" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2270" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;exitX=0;exitY=0.5;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="556" y="747.4999999999999" as="sourcePoint" />
            <mxPoint x="473" y="643" as="targetPoint" />
            <Array as="points">
              <mxPoint x="513" y="748" />
              <mxPoint x="473" y="748" />
            </Array>
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2274" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;entryX=1;entryY=0.5;entryDx=0;entryDy=0;entryPerimeter=0;exitX=0;exitY=0.5;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="564" y="952.71" as="sourcePoint" />
            <mxPoint x="367" y="952.71" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2275" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;exitX=0.5;exitY=0;exitDx=0;exitDy=0;entryX=0.5;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1" target="2093">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="473" y="838" as="sourcePoint" />
            <mxPoint x="463" y="782" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2276" value="&lt;font color=&quot;#23445d&quot;&gt;PostgreSQL&amp;nbsp;cluster&amp;nbsp;&lt;/font&gt;" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=none;fontSize=14;fontColor=#742B21;align=center;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="503" y="848" width="139" height="19" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2278" value="PostgreSQL [nod_1]" style="shape=mxgraph.cisco.storage.relational_database;sketch=0;html=1;pointerEvents=1;dashed=0;fillColor=#036897;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;align=center;outlineConnect=0;" vertex="1" parent="1">
          <mxGeometry x="313" y="926.5" width="66" height="53" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2282" value="&lt;div style=&quot;line-height: 0%;&quot;&gt;&lt;span style=&quot;font-size: 14px; background-color: initial;&quot;&gt;&lt;font color=&quot;#000000&quot;&gt;jira [nod_2]&lt;/font&gt;&lt;/span&gt;&lt;br&gt;&lt;/div&gt;" style="shape=mxgraph.cisco.servers.fileserver;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=36;fontColor=#FFB366" vertex="1" parent="1">
          <mxGeometry x="567.5" y="613.5" width="43" height="62" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2283" value="PostgreSQL [nod_2]" style="shape=mxgraph.cisco.storage.relational_database;sketch=0;html=1;pointerEvents=1;dashed=0;fillColor=#036897;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;align=center;outlineConnect=0;" vertex="1" parent="1">
          <mxGeometry x="567.5" y="932" width="66" height="53" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2284" value="nfs" style="shape=mxgraph.cisco.storage.relational_database;sketch=0;html=1;pointerEvents=1;dashed=0;fillColor=#036897;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;align=center;outlineConnect=0;" vertex="1" parent="1">
          <mxGeometry x="556" y="720" width="66" height="53" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2287" value="&lt;font color=&quot;#23445d&quot;&gt;Balancer&lt;/font&gt;" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=none;fontSize=14;fontColor=#742B21;align=center;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="524" y="369" width="139" height="19" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2289" value="&lt;font color=&quot;#23445d&quot;&gt;WEB&lt;/font&gt;" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=none;fontSize=14;fontColor=#742B21;align=center;fontStyle=1" vertex="1" parent="1">
          <mxGeometry x="564.5" y="316" width="139" height="19" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2291" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;entryX=0.5;entryY=1;entryDx=0;entryDy=0;" edge="1" parent="1" target="Xr0FSyJAFfYrDeTETw8K-2285">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="473" y="560" as="sourcePoint" />
            <mxPoint x="483" y="808" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2294" style="edgeStyle=elbowEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;elbow=vertical;html=1;exitX=0.5;exitY=1;exitDx=0;exitDy=0;" edge="1" parent="1">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="1213.5" y="750" as="sourcePoint" />
            <mxPoint x="1213.5" y="750" as="targetPoint" />
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2301" value="" style="rounded=1;whiteSpace=wrap;html=1;strokeColor=none;fillColor=#BAC8D3;fontSize=24;fontColor=#23445D;align=center;opacity=60;" vertex="1" parent="1">
          <mxGeometry x="990" y="298" width="380" height="402" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2303" value="Monitoring" style="shape=mxgraph.cisco.servers.fileserver;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=14;fontColor=#000000;" vertex="1" parent="1">
          <mxGeometry x="1174" y="335" width="43" height="62" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2304" value="BorgBackup" style="shape=mxgraph.cisco.servers.fileserver;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=14;fontColor=#000000;" vertex="1" parent="1">
          <mxGeometry x="1174" y="450" width="43" height="62" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2305" value="ELK_Stack" style="shape=mxgraph.cisco.servers.fileserver;html=1;dashed=0;fillColor=#10739E;strokeColor=#ffffff;strokeWidth=2;verticalLabelPosition=bottom;verticalAlign=top;fontFamily=Helvetica;fontSize=14;fontColor=#000000;" vertex="1" parent="1">
          <mxGeometry x="1174" y="568" width="43" height="62" as="geometry" />
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2311" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;" edge="1" parent="1" source="Xr0FSyJAFfYrDeTETw8K-2305" target="2138">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="1219" y="462.4999999999999" as="sourcePoint" />
            <mxPoint x="1136" y="358" as="targetPoint" />
            <Array as="points">
              <mxPoint x="1130" y="600" />
              <mxPoint x="990" y="600" />
              <mxPoint x="830" y="600" />
            </Array>
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2312" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;entryX=0.503;entryY=0.965;entryDx=0;entryDy=0;entryPerimeter=0;" edge="1" parent="1" target="2138">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="1170" y="483" as="sourcePoint" />
            <mxPoint x="830" y="210" as="targetPoint" />
            <Array as="points">
              <mxPoint x="1130" y="483" />
              <mxPoint x="990" y="483" />
              <mxPoint x="830" y="483" />
            </Array>
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2313" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;entryX=0.505;entryY=0.978;entryDx=0;entryDy=0;entryPerimeter=0;exitX=-0.023;exitY=0.551;exitDx=0;exitDy=0;exitPerimeter=0;" edge="1" parent="1" source="Xr0FSyJAFfYrDeTETw8K-2303" target="2138">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="1219" y="368" as="sourcePoint" />
            <mxPoint x="830" y="230" as="targetPoint" />
            <Array as="points">
              <mxPoint x="1130" y="369" />
              <mxPoint x="990" y="369" />
              <mxPoint x="830" y="369" />
            </Array>
          </mxGeometry>
        </mxCell>
        <mxCell id="Xr0FSyJAFfYrDeTETw8K-2314" style="edgeStyle=none;rounded=1;html=1;strokeColor=#23445D;endArrow=none;endFill=0;strokeWidth=4;exitX=1;exitY=0.497;exitDx=0;exitDy=0;exitPerimeter=0;entryX=0.497;entryY=0.983;entryDx=0;entryDy=0;entryPerimeter=0;" edge="1" parent="1" source="Xr0FSyJAFfYrDeTETw8K-2288" target="2138">
          <mxGeometry relative="1" as="geometry">
            <mxPoint x="710" y="699" as="sourcePoint" />
            <mxPoint x="826.5" y="215.94" as="targetPoint" />
            <Array as="points">
              <mxPoint x="827" y="699" />
              <mxPoint x="827" y="640" />
              <mxPoint x="827.5" y="608.94" />
            </Array>
          </mxGeometry>
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>



