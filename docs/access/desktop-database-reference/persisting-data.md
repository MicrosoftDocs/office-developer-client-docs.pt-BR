---
title: Mantendo dados (referência de banco de dados da área de trabalho do Access)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f5788216a20e62cfc39fd2081f4f672bc4f9b808
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713958"
---
# <a name="persisting-data"></a>Dados persistentes


**Aplica-se a**: Access 2013, o Office 2013

A computação portátil (por exemplo, a utilização de laptops) gerou a necessidade de aplicativos que possam ser executados conectados e desconectados. O ADO adicionou suporte a isso, permitindo ao desenvolvedor salvar um **Recordset** de cursor do cliente no disco e recarregá-lo posteriormente.

Há vários cenários nos quais você poderia usar esse tipo de recurso, incluindo os seguintes:

- **Viagens:** ao levar o aplicativo em viagem, é essencial fornecer a capacidade de fazer alterações e adicionar novos registros que possam ser posteriormente reconectados ao banco de dados e confirmados.

- **Pesquisas atualizadas raramente:** Frequentemente em um aplicativo as tabelas são usadas como pesquisas  por exemplo, as tabelas de impostos estaduais. Elas são atualizadas raramente e são somente leitura. Em vez de reler esses dados do servidor cada vez que o aplicativo é iniciado, ele pode simplesmente carregar os dados de um **Recordset** mantido localmente.

No ADO, para salvar e carregar **Recordsets**, use os métodos **Recordset.Save** e **Recordset.Open(,,,,adCmdFile)** no objeto **Recordset** do ADO.

Você pode usar o método **Save** do **Recordset** para manter o **Recordset** do ADO em um arquivo em um disco. (Também é possível salvar um **Recordset** em um objeto **Stream** do ADO. Os objetos **Stream** são abordados posteriormente no guia.) Depois, você pode usar o método **Open** para abrir o **Recordset** novamente quando estiver pronto para usá-lo. Por padrão, o ADO salva o **Recordset** no formato Microsoft Advanced Data TableGram (ADTG) proprietário. Esse formato binário é especificado usando o valor **adPersistADTG** **PersistFormatEnum**. Alternativamente, você pode salvar seu **Recordset** fora, como XML, em vez de usar o **adPersistXML**. Para obter mais informações sobre como salvar Recordsets como XML, consulte [Mantendo registros em formato XML](persisting-records-in-xml-format.md).

A sintaxe do método **Save** é a seguinte:

`recordset.Save Destination, PersistFormat`

Na primeira vez que você salva o **Recordset**, é opcional especificar *Destination*. Se você omitir *Destination*, será criado um novo arquivo com o nome definido como o valor da propriedade [Source](source-property-ado-recordset.md) do **Recordset**.

Omita *Destination* ao chamar **Save** subsequentemente após o primeiro salvamento, ou ocorrerá um erro em tempo de execução. Se você chamar **Save** subsequentemente com um novo *Destination*, o **Recordset** será salvo no novo destino. Contudo, o novo destino e o destino original serão abertos.

**Save** não fecha o **Recordset** ou *Destination*, então você poderá continuar trabalhando com o **Recordset** e salvar suas alterações mais recentes. *Destination* permanecerá aberto até que o **Recordset** seja fechado e, durante esse tempo, outros aplicativos poderá ler mas não gravar em *Destination*.

Por motivos de segurança, o método **Save** permite apenas a utilização de definições de segurança baixas e personalizadas a partir de um script executado pelo Microsoft Internet Explorer. Para obter uma explicação mais detalhada dos problemas de segurança, consulte "ADO and RDS Security Issues in Microsoft Internet Explorer" sob Artigos Técnicos do ActiveX Data Objects (ADO) nos Artigos Técnicos de Acesso a Dados da Microsoft.

Se o método **Save** for chamado enquanto uma operação de busca, execução ou atualização assíncrona de **Recordset** estiver em andamento, **Save** aguardará até que a operação assíncrona seja concluída.

Os registros são salvos a partir da primeira linha do **Recordset**. Quando o método **Save** for concluído, a posição de linha atual será movida para a primeira linha do **Recordset**.

Para obter melhores resultados, defina a propriedade [CursorLocation](cursorlocation-property-ado.md) para **adUseClient** com **Save**. Se o provedor não oferecer suporte a toda a funcionalidade necessária para salvar objetos **Recordset**, o Cursor Service fornecerá essa funcionalidade.

Quando um **Recordset** for mantido com a propriedade **CursorLocation** definida como **adUseServer**, a capacidade de atualização do **Recordset** será limitada. Normalmente, apenas atualizações, inserções e exclusões de tabela única são permitidas (dependendo da funcionalidade do provedor). O método [Resync](resync-method-ado.md) também está indisponível nessa configuração.

Porque o parâmetro *Destination* pode aceitar qualquer objeto que dá suporte à interface **IStream** do OLE DB, você pode salvar um **Recordset** diretamente para o objeto de **resposta** do ASP.

No exemplo a seguir, os métodos **Save** e **Open** são usados para manter um **Recordset** e reabri-lo posteriormente:

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

Esta seção inclui os seguintes tópicos:

- [Mais informações sobre a persistência de Recordset](more-about-recordset-persistence.md)

- [Mantendo Recordsets hierárquicos e filtrados](persisting-filtered-and-hierarchical-recordsets.md)

- [Mantendo registros em formato XML (ADO)](persisting-records-in-xml-format.md)
