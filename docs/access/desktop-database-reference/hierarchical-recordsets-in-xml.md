---
title: Objetos Recordset hierárquicos em XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f608cd8ed36b621847c58dd523cfa052c5f501a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464351"
---
# <a name="hierarchical-recordsets-in-xml"></a>Objetos Recordset hierárquicos em XML


**Aplica-se a**: Access 2013 | Office 2013

## <a name="hierarchical-recordsets-in-xml"></a>Objetos Recordset hierárquicos em XML

O ADO permite a persistência de objetos **Recordset** hierárquicos em XML. Com objetos **Recordset** hierárquicos, o valor de um campo no **Recordset** pai é outro **Recordset**. Tais campos são representados como elementos filho no fluxo XML, e não como um atributo. O exemplo a seguir demonstra esse caso:

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

Veja a seguir o formato XML do **Recordset** persistente:

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

A ordem exata das colunas no **Recordset** pai não é óbvia quando ela mantida dessa maneira. Qualquer campo do pai pode conter um **Recordset** filho. O Persistence Provider mantém primeiro todas as colunas escalares como atributos e, em seguida, mantém todas as "colunas" do **Recordset** como elementos filho da linha pai. A posição ordinal do campo no **Recordset** pai pode ser obtida por meio da definição do esquema do **Recordset**. Todos os campos têm uma propriedade OLE DB, **rs:number**, definida no namespace do esquema do **Recordset** que contém o número ordinal desse campo.

Os nomes de todos os campos no **Recordset** filho são concatenados com o nome do campo no **Recordset** pai que contém esse filho. Isso garante que não haja conflitos de nomes nos casos em que os objetos **Recordset** pai e filho contêm um campo obtido de duas tabelas diferentes, porém, com um único nome.

Ao salvar objetos **Recordset** hierárquicos em XML, lembre-se das seguintes restrições do ADO:

  - Um **Recordset** hierárquico com atualizações pendentes não pode ser mantido em XML.

  - Um **Recordset** hierárquico criado com um comando shape parametrizado não pode ser mantido (seja no formato XML ou no formato ADTG).

  - O ADO salva a relação entre o pai e os objetos **Recordset** filho como um BLOB (objeto grande binário). As marcas XML usadas para descrever essa relação ainda não foram definidas no namespace do esquema do conjunto de linhas.

  - Quando um **Recordset** hierárquico é salvo, todos os **Recordsets** filho são salvos com ele. Se o **Recordset** atual for filho de outro **Recordset**, seu pai não será salvo. Contudo, serão salvos todos os **Recordsets** filho que formam a subárvore do **Recordset**.

Quando um **Recordset** for reaberto em seu formato persistente XML, lembre-se das seguintes limitações:

  - Se o registro filho contiver registros para os quais não haja registros pai correspondentes, essas linhas não serão gravadas na representação XML do **Recordset** hierárquico. Portanto, elas serão perdidas quando o **Recordset** for reaberto em seu local persistente.

  - Se um registro filho fizer referência a mais de um registro pai, na reabertura do **Recordset**, o **Recordset** filho poderá conter registros duplicados. Contudo, essas duplicatas só ficarão visíveis se o usuário trabalhar diretamente com o conjunto de linhas filho subjacente. Se um capítulo for usado para navegar pelo **Recordset** filho (essa é a única maneira de navegar pelo ADO), as duplicatas não ficarão visíveis.

