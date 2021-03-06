---
title: Registros persistentes no formato XML
TOCTitle: Persisting records in XML format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 10a5651c74580950810211c4f71e19fc80a16a95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287563"
---
# <a name="persisting-records-in-xml-format"></a>Registros persistentes no formato XML

**Aplica-se ao:** Access 2013, Office 2013

Como no formato ADTG, a manutenção de **Recordset** no formato XML é implementada com o Microsoft OLE DB Persistence Provider. Esse provedor gera um conjunto de linhas somente leitura, somente de encaminhamento a partir de um fluxo ou arquivo XML salvo que contém as informações de esquema geradas pelo ADO. Da mesma maneira, ele pode pegar um **Recordset** do ADO, gerar o XML e salvá-lo em um arquivo ou em qualquer objeto que implemente a interface **IStream** do COM. (Na verdade, um arquivo é apenas outro exemplo de um objeto que oferece suporte ao **IStream**.) Para as versões 2.5 e posteriores, o ADO se baseia no Microsoft XML Parser (MSXML) para carregar o XML no **Recordset**; portanto, o msxml.dll é necessário. Para a versão 2.5, o MSXML foi fornecido com o Internet Explorer 5. Para a versão 2.6, o MSXML foi fornecido com o SQL Server 2000.

> [!NOTE]
> [!OBSERVAçãO] Algumas limitações de aplicam ao salvar **Recordsets** hierárquicos (formas de dados) em formato XML. Não será possível salvar em XML se o **Recordset** hierárquico contiver atualizações pendentes e não será possível salvar um **Recordset** hierárquico com parâmetros. Para obter mais informações, consulte [Recordsets hierárquicos em XML](hierarchical-recordsets-in-xml.md).


A maneira mais fácil de manter dados em XML e carregá-los novamente através do ADO é com os métodos **Save** e **Open**, respectivamente. O exemplo de código do ADO a seguir demonstra como salvar os dados da tabela Titles em um arquivo nomeado titles.sav.

```vb 
 
Dim rs as new Recordset 
Dim rs2 as new Recordset 
Dim c as new Connection 
Dim s as new Stream 
 
' Query the Titles table. 
c.Open "provider='sqloledb';data source='mydb';initial catalog='pubs';Integrated Security='SSPI'" 
rs.cursorlocation = adUseClient 
rs.Open "select * from titles", c, adOpenStatic 
 
' Save to the file in the XML format. Note that if you don't specify 
' adPersistXML, a binary format (ADTG) will be used by default. 
rs.Save "titles.sav", adPersistXML 
 
' Save the Recordset into the ADO Stream object. 
rs.save s, adPersistXML 
rs.Close 
c.Close 
 
set rs = nothing 
 
Reopen the file. 
rs.Open "titles.sav",,,,adCmdFile 
'Open the Stream back into a Recordset. 
rs2.open s 
```

O ADO sempre mantém todo o objeto **Recordset**. Se você deseja manter apenas um subconjunto de linhas do objeto **Recordset**, use o método **Filter** para estreitar as linhas ou alterar sua cláusula de seleção. No entanto, você deve abrir um objeto **Recordset** com um cursor do lado do cliente (**CursorLocation**  =  **adUseClient**) para usar o método **Filter** para salvar um subconjunto de linhas. Por exemplo, para recuperar títulos que começam com a letra "b," você pode aplicar um filtro a um objeto **Recordset** aberto:

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

O ADO sempre usa o conjunto de linhas do Mecanismo de cursor do cliente para produzir um objeto **Recordset** que pode ser rolado e indicado sobre os dados somente de encaminhamento gerados pelo Persistence Provider.

Esta seção inclui os seguintes tópicos:

- [Formato de persistência XML](xml-persistence-format.md)

- [Namespaces](namespaces.md)

- [Seção Schema](schema-section.md)

- [Seção Data](data-section.md)

- [Conjuntos de registros hierárquicos em XML](hierarchical-recordsets-in-xml.md)

- [Propriedades dinâmicas do Recordset em XML](recordset-dynamic-properties-in-xml.md)

- [Transformações XSLT](xslt-transformations.md)

- [Salvando no objeto DOM XML](saving-to-the-xml-dom-object.md)

- [Considerações sobre segurança XML](xml-security-considerations.md)

- [Tópicos do cenário de persistência do recordset XML](xml-recordset-persistence-scenario.md)
