---
title: Fazendo uma conexão
TOCTitle: Making a Connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bd99419a841a8fa876dd0ad30b4d06360a27df1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882046"
---
# <a name="making-a-connection"></a>Fazendo uma conexão

**Aplica-se a**: Access 2013, o Office 2013

Para se conectar à fonte de dados, especifique uma *sequência de caracteres de conexão* e os parâmetros para diferenciar cada provedor ou fonte de dados. Para obter mais informações, consulte [Criando uma sequência de caracteres de conexão](creating-the-connection-string.md).

Geralmente, o ADO abre uma conexão usando o objeto **Connection** do método **Open**. A sintaxe do método **Open** é apresentada a seguir:

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

De forma alternativa, você pode chamar a técnica de atalho, **Recordset.Open**, para abrir uma conexão implícita e emitir um comando sobre aquela conexão em uma operação. Faça isso passando uma cadeia de caracteres de conexão válida como o argumento *ActiveConnection* do método **Open** . Esta é a sintaxe de cada método do Visual Basic:

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!OBSERVAçãO] Quando devo usar um objeto **Connection** versus o atalho **Recordset.Open** ? Use o objeto **Connection** se você planeja abrir mais de um **Recordset** ou quando executar vários comandos. Uma conexão ainda será criada pelo ADO de forma implícita, quando você usar o atalho **Recordset.Open**.


