---
title: Objetos Recordset hierárquicos em XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e0aafaa1f7f49d34d647ec0f733e68de21cb5369
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292010"
---
# <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="7aa2a-102">Conjuntos de registros hierárquicos em XML</span><span class="sxs-lookup"><span data-stu-id="7aa2a-102">Hierarchical Recordsets in XML</span></span>


<span data-ttu-id="7aa2a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7aa2a-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="7aa2a-104">Objetos Recordset hierárquicos em XML</span><span class="sxs-lookup"><span data-stu-id="7aa2a-104">Hierarchical Recordsets in XML</span></span>

<span data-ttu-id="7aa2a-p101">O ADO permite a persistência de objetos **Recordset** hierárquicos em XML. Com objetos **Recordset** hierárquicos, o valor de um campo no **Recordset** pai é outro **Recordset**. Tais campos são representados como elementos filho no fluxo XML, e não como um atributo. O exemplo a seguir demonstra esse caso:</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p101">ADO allows persistence of hierarchical **Recordset** objects into XML. With hierarchical **Recordset** objects, the value of a field in the parent **Recordset** is another **Recordset**. Such fields are represented as child elements in the XML stream rather than an attribute. The following example demonstrates this case:</span></span>

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

<span data-ttu-id="7aa2a-109">Veja a seguir o formato XML do **Recordset** persistente:</span><span class="sxs-lookup"><span data-stu-id="7aa2a-109">The following is the XML format of the persisted **Recordset**:</span></span>

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

<span data-ttu-id="7aa2a-p102">A ordem exata das colunas no **Recordset** pai não é óbvia quando ela mantida dessa maneira. Qualquer campo do pai pode conter um **Recordset** filho. O Persistence Provider mantém primeiro todas as colunas escalares como atributos e, em seguida, mantém todas as "colunas" do **Recordset** como elementos filho da linha pai. A posição ordinal do campo no **Recordset** pai pode ser obtida por meio da definição do esquema do **Recordset**. Todos os campos têm uma propriedade OLE DB, **rs:number**, definida no namespace do esquema do **Recordset** que contém o número ordinal desse campo.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p102">The exact order of the columns in the parent **Recordset** is not obvious when it is persisted in this manner. Any field in the parent may contain a child **Recordset**. The Persistence Provider persists out all scalar columns first as attributes and then persists out all child **Recordset** "columns" as child elements of the parent row. The ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset**. Every field has an OLE DB property, **rs:number**, defined in the **Recordset** schema namespace that contains the ordinal number for that field.</span></span>

<span data-ttu-id="7aa2a-p103">Os nomes de todos os campos no **Recordset** filho são concatenados com o nome do campo no **Recordset** pai que contém esse filho. Isso garante que não haja conflitos de nomes nos casos em que os objetos **Recordset** pai e filho contêm um campo obtido de duas tabelas diferentes, porém, com um único nome.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p103">The names of all fields in the child **Recordset** are concatenated with the name of the field in the parent **Recordset** that contains this child. This is to ensure that there are no name collisions in cases where parent and child **Recordsets** both contain a field that is obtained from two different tables but is named singularly.</span></span>

<span data-ttu-id="7aa2a-117">Ao salvar objetos **Recordset** hierárquicos em XML, lembre-se das seguintes restrições do ADO:</span><span class="sxs-lookup"><span data-stu-id="7aa2a-117">When saving hierarchical **Recordsets** into XML, you should be aware of the following restrictions in ADO:</span></span>

  - <span data-ttu-id="7aa2a-118">Um **Recordset** hierárquico com atualizações pendentes não pode ser mantido em XML.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-118">A hierarchical **Recordset** with pending updates cannot be persisted into XML.</span></span>

  - <span data-ttu-id="7aa2a-119">Um **Recordset** hierárquico criado com um comando shape parametrizado não pode ser mantido (seja no formato XML ou no formato ADTG).</span><span class="sxs-lookup"><span data-stu-id="7aa2a-119">A hierarchical **Recordset** created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</span></span>

  - <span data-ttu-id="7aa2a-p104">O ADO salva a relação entre o pai e os objetos **Recordset** filho como um BLOB (objeto grande binário). As marcas XML usadas para descrever essa relação ainda não foram definidas no namespace do esquema do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p104">ADO currently saves the relationship between the parent and the child **Recordsets** as a binary large object (BLOB). XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</span></span>

  - <span data-ttu-id="7aa2a-p105">Quando um **Recordset** hierárquico é salvo, todos os **Recordsets** filho são salvos com ele. Se o **Recordset** atual for filho de outro **Recordset**, seu pai não será salvo. Contudo, serão salvos todos os **Recordsets** filho que formam a subárvore do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p105">When a hierarchical **Recordset** is saved, all child **Recordsets** are saved along with it. If the current **Recordset** is a child of another **Recordset**, its parent is not saved. All child **Recordsets** that form the subtree of the current **Recordset** are saved.</span></span>

<span data-ttu-id="7aa2a-125">Quando um **Recordset** for reaberto em seu formato persistente XML, lembre-se das seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="7aa2a-125">When a hierarchical **Recordset** is reopened from its XML-persisted format, you must be aware of the following limitations:</span></span>

  - <span data-ttu-id="7aa2a-p106">Se o registro filho contiver registros para os quais não haja registros pai correspondentes, essas linhas não serão gravadas na representação XML do **Recordset** hierárquico. Portanto, elas serão perdidas quando o **Recordset** for reaberto em seu local persistente.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p106">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical **Recordset**. Thus, these rows will be lost when the **Recordset** is reopened from its persisted location.</span></span>

  - <span data-ttu-id="7aa2a-p107">Se um registro filho fizer referência a mais de um registro pai, na reabertura do **Recordset**, o **Recordset** filho poderá conter registros duplicados. Contudo, essas duplicatas só ficarão visíveis se o usuário trabalhar diretamente com o conjunto de linhas filho subjacente. Se um capítulo for usado para navegar pelo **Recordset** filho (essa é a única maneira de navegar pelo ADO), as duplicatas não ficarão visíveis.</span><span class="sxs-lookup"><span data-stu-id="7aa2a-p107">If a child record has references to more than one parent record, then on reopening the **Recordset**, the child **Recordset** may contain duplicate records. However, these duplicates will only be visible if the user works directly with the underlying child rowset. If a chapter is used to navigate the child **Recordset** (that is the only way to navigate through ADO), the duplicates are not visible.</span></span>

