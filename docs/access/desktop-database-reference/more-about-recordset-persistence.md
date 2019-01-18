---
title: Mais informações sobre a persistência do conjunto de registros
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717605"
---
# <a name="more-about-recordset-persistence"></a><span data-ttu-id="4d49c-102">Mais informações sobre a persistência do conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="4d49c-102">More about Recordset persistence</span></span>

<span data-ttu-id="4d49c-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d49c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d49c-104">O objeto Recordset do ADO oferece suporte ao repositório do conteúdo de um objeto **Recordset** em arquivo por meio de seu método [Save](save-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4d49c-104">The ADO Recordset object supports storing a **Recordset** object's contents in a file using its [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="4d49c-105">O arquivo persistentemente armazenado pode existir em uma unidade local, o servidor de rede, ou como uma URL em um site.</span><span class="sxs-lookup"><span data-stu-id="4d49c-105">The persistently stored file may exist on a local drive, network server, or as a URL on a website.</span></span> <span data-ttu-id="4d49c-106">Posteriormente, o arquivo poderá ser restaurado com o método **Open** do objeto [Recordset](open-method-ado-recordset.md) ou com o método [Execute](connection-object-ado.md) do objeto [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection).</span><span class="sxs-lookup"><span data-stu-id="4d49c-106">Later, the file can be restored with either the **Recordset** object's [Open](open-method-ado-recordset.md) method or the [Connection](connection-object-ado.md) object's [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method.</span></span>

<span data-ttu-id="4d49c-107">O método [GetString](getstring-method-ado.md) também converte um objeto **Recordset** em uma forma na qual as colunas e as linhas são delimitadas pelos caracteres especificados.</span><span class="sxs-lookup"><span data-stu-id="4d49c-107">In addition, the [GetString](getstring-method-ado.md) method converts a **Recordset** object to a form in which the columns and rows are delimited with characters you specify.</span></span>

<span data-ttu-id="4d49c-p102">Para manter um **Recordset**, comece convertendo-o em uma forma que possa ser armazenada em um arquivo. Os objetos **Recordset** podem ser armazenados no formato ADTG (Advanced Data TableGram) proprietário ou no formato XML aberto. Os exemplos de ADTG são mostrados a seguir. Para obter mais informações sobre a persistência XML, consulte [Mantendo registros em formato XML](persisting-records-in-xml-format.md).</span><span class="sxs-lookup"><span data-stu-id="4d49c-p102">To persist a **Recordset**, begin by converting it to a form that can be stored in a file. **Recordset** objects can be stored in the proprietary Advanced Data TableGram (ADTG) format or the open Extensible Markup Language (XML) format. ADTG examples are shown below. For more information about XML persistence, see [Persisting Records in XML format](persisting-records-in-xml-format.md).</span></span>

<span data-ttu-id="4d49c-p103">Salve todas as alterações pendentes no arquivo persistente. Esse procedimento permitirá emitir uma consulta que retorna um objeto **Recordset**, edita o **Recordset**, salva esse objeto e as alterações pendentes, restaura posteriormente o **Recordset** e, em seguida, atualiza a fonte de dados com as alterações pendentes salvas.</span><span class="sxs-lookup"><span data-stu-id="4d49c-p103">Save any pending changes in the persisted file. Doing this allows you to issue a query that returns a **Recordset** object, edits the **Recordset**, saves it and the pending changes, later restores the **Recordset**, and then updates the data source with the saved pending changes.</span></span>

<span data-ttu-id="4d49c-114">Para obter informações sobre como armazenar objetos **Stream** de forma persistente, consulte [Objetos Stream e persistência](streams-and-persistence.md) no capítulo 10.</span><span class="sxs-lookup"><span data-stu-id="4d49c-114">For information about persistently storing **Stream** objects, see [Streams and Persistence](streams-and-persistence.md) in Chapter 10.</span></span>

<span data-ttu-id="4d49c-115">Para obter um exemplo de persistência de **Recordset**, consulte [Cenário de persistência de um conjunto de registros XML](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="4d49c-115">For an example of **Recordset** persistence, see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

## <a name="example"></a><span data-ttu-id="4d49c-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4d49c-116">Example</span></span>

<span data-ttu-id="4d49c-117">**Salvar um Recordset:**</span><span class="sxs-lookup"><span data-stu-id="4d49c-117">**Save a Recordset:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

<span data-ttu-id="4d49c-118">**Abrir um arquivo persistente com Recordset.Open:**</span><span class="sxs-lookup"><span data-stu-id="4d49c-118">**Open a persisted file with Recordset.Open:**</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

<span data-ttu-id="4d49c-119">Opcionalmente, se **Recordset** não tiver conexão ativa, você poderá aceitar todos os padrões e simplesmente gerar este código:</span><span class="sxs-lookup"><span data-stu-id="4d49c-119">Optionally, if the **Recordset** does not have an active connection, you can accept all the defaults and simply code the following:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

<span data-ttu-id="4d49c-120">**Abrir um arquivo persistente com Connection.Execute:**</span><span class="sxs-lookup"><span data-stu-id="4d49c-120">**Open a persisted file with Connection.Execute:**</span></span>

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

<span data-ttu-id="4d49c-121">**Abrir um arquivo persistente com RDS.DataControl:**</span><span class="sxs-lookup"><span data-stu-id="4d49c-121">**Open a persisted file with RDS.DataControl:**</span></span>

<span data-ttu-id="4d49c-122">Neste caso, a propriedade **Server** não está definida.</span><span class="sxs-lookup"><span data-stu-id="4d49c-122">In this case, the **Server** property is not set.</span></span>

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

