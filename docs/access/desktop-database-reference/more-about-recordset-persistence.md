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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288845"
---
# <a name="more-about-recordset-persistence"></a>Mais informações sobre a persistência do conjunto de registros

**Aplica-se ao:** Access 2013, Office 2013

O objeto Recordset do ADO oferece suporte ao repositório do conteúdo de um objeto **Recordset** em arquivo por meio de seu método [Save](save-method-ado.md). O arquivo armazenado de forma persistente pode existir em uma unidade local, servidor de rede ou como uma URL em um site. Posteriormente, o arquivo poderá ser restaurado com o método **Open** do objeto [Recordset](open-method-ado-recordset.md) ou com o método [Execute](connection-object-ado.md) do objeto [Connection](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection).

O método [GetString](getstring-method-ado.md) também converte um objeto **Recordset** em uma forma na qual as colunas e as linhas são delimitadas pelos caracteres especificados.

Para manter um **Recordset**, comece convertendo-o em uma forma que possa ser armazenada em um arquivo. Os objetos **Recordset** podem ser armazenados no formato ADTG (Advanced Data TableGram) proprietário ou no formato XML aberto. Os exemplos de ADTG são mostrados a seguir. Para obter mais informações sobre a persistência XML, consulte [Mantendo registros em formato XML](persisting-records-in-xml-format.md).

Salve todas as alterações pendentes no arquivo persistente. Esse procedimento permitirá emitir uma consulta que retorna um objeto **Recordset**, edita o **Recordset**, salva esse objeto e as alterações pendentes, restaura posteriormente o **Recordset** e, em seguida, atualiza a fonte de dados com as alterações pendentes salvas.

Para obter informações sobre como armazenar objetos **Stream** de forma persistente, consulte [Objetos Stream e persistência](streams-and-persistence.md) no capítulo 10.

Para obter um exemplo de persistência de **Recordset**, consulte [Cenário de persistência de um conjunto de registros XML](xml-recordset-persistence-scenario.md).

## <a name="example"></a>Exemplo

**Salvar um Recordset:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Abrir um arquivo persistente com Recordset.Open:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

Opcionalmente, se **Recordset** não tiver conexão ativa, você poderá aceitar todos os padrões e simplesmente gerar este código:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Abrir um arquivo persistente com Connection.Execute:**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Abrir um arquivo persistente com RDS.DataControl:**

Neste caso, a propriedade **Server** não está definida.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

