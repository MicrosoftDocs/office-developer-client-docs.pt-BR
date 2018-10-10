---
title: Mantendo registros em formato XML
TOCTitle: Persisting Records in XML Format
ms:assetid: 8071e244-60c7-759c-094c-152add5d72e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249545(v=office.15)
ms:contentKeyID: 48545924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b1e22c3f85c4289520326c34c6d0c218a442a3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463818"
---
# <a name="persisting-records-in-xml-format"></a>Mantendo registros em formato XML


**Aplica-se a**: Access 2013 | Office 2013

Como no formato ADTG, a manutenção de **Recordset** no formato XML é implementada com o Microsoft OLE DB Persistence Provider. Esse provedor gera um conjunto de linhas somente leitura, somente de encaminhamento a partir de um fluxo ou arquivo XML salvo que contém as informações de esquema geradas pelo ADO. Da mesma maneira, ele pode pegar um **Recordset** do ADO, gerar o XML e salvá-lo em um arquivo ou em qualquer objeto que implemente a interface **IStream** do COM. (Na verdade, um arquivo é apenas outro exemplo de um objeto que oferece suporte ao **IStream**.) Para as versões 2.5 e posteriores, o ADO se baseia no Microsoft XML Parser (MSXML) para carregar o XML no **Recordset**; portanto, o msxml.dll é necessário. Para a versão 2.5, o MSXML foi fornecido com o Internet Explorer 5. Para a versão 2.6, o MSXML foi fornecido com o SQL Server 2000.


> [!NOTE]
> <P>[!OBSERVAçãO] Algumas limitações de aplicam ao salvar <STRONG>Recordsets</STRONG> hierárquicos (formas de dados) em formato XML. Não será possível salvar em XML se o <STRONG>Recordset</STRONG> hierárquico contiver atualizações pendentes e não será possível salvar um <STRONG>Recordset</STRONG> hierárquico com parâmetros. Para obter mais informações, consulte <A href="hierarchical-recordsets-in-xml.md">Recordsets hierárquicos em XML</A>.</P>



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

O ADO sempre mantém todo o objeto **Recordset**. Se você deseja manter apenas um subconjunto de linhas do objeto **Recordset**, use o método **Filter** para estreitar as linhas ou alterar sua cláusula de seleção. No entanto, é necessário abrir um objeto **Recordset** com um cursor do cliente (**CursorLocation** = **adUseClient**) usar o método de **filtro** para salvar um subconjunto de linhas. Por exemplo, para recuperar títulos que começam com a letra "b," você pode aplicar um filtro a um objeto **Recordset** aberto:

```vb 
 
rs.Filter "title_id like 'B*'" 
rs.Save "btitles.sav", adPersistXML 
```

O ADO sempre usa o conjunto de linhas do Mecanismo de cursor do cliente para produzir um objeto **Recordset** que pode ser rolado e indicado sobre os dados somente de encaminhamento gerados pelo Persistence Provider.

