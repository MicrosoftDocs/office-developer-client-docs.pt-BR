---
title: Objeto Connection (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ed736a0e52ff45cd0fed63f1ba5bd7060d7a2380
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295874"
---
# <a name="connection-object-ado"></a>Objeto Connection (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Representa uma conexão aberta com uma fonte de dados.

## <a name="remarks"></a>Comentários

Um objeto **Connection** representa uma única sessão com uma fonte de dados. No caso de um sistema de banco de dados cliente/servidor, pode ser equivalente à conexão de rede real com o servidor. Dependendo da funcionalidade suportada pelo provedor, algumas coleções, métodos ou propriedades de um objeto **Connection** podem não estar disponíveis.

Com as coleções, os métodos e as propriedades de um objeto **Connection**, você pode fazer o seguinte:

  - Configurar a conexão antes de abri-la com as propriedades [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md) e [Mode](mode-property-ado.md). **ConnectionString** é a propriedade padrão de um objeto **Connection**.

  - Definir a propriedade [CursorLocation](cursorlocation-property-ado.md) para o cliente chamar o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), que suporta as atualizações em lotes.

  - Definir o banco de dados padrão da conexão com a propriedade [DefaultDatabase](defaultdatabase-property-ado.md).

  - Definir o nível de isolamento das transações abertas na conexão com a propriedade [IsolationLevel](isolationlevel-property-ado.md).

  - Especificar um provedor do OLE DB com a propriedade [Provider](provider-property-ado.md).

  - Estabelecer, e mais tarde quebrar, a conexão física da fonte de dados com os métodos [Open](open-method-ado-connection.md) e [Close](close-method-ado.md).

  - Executar um comando na conexão com o método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) e configurar a execução com a propriedade [CommandTimeout](commandtimeout-property-ado.md).
    
    > [!NOTE]
    > [!OBSERVAçãO] Para executar uma consulta sem usar o objeto Command, passe uma sequência de consulta para o método **Execute** de um objeto **Connection**. No entanto, um objeto [Command](command-object-ado.md) será necessário quando você desejar insistir no texto de comando e reexecutá-lo ou usar os parâmetros da consulta.

  - Gerenciar as transações na conexão aberta, incluindo as transações aninhadas se o provedor oferecer suporte para essas transações, com o métodos [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) e [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) e a propriedade [Attributes](attributes-property-ado.md).

  - Examinar os erros retornados da fonte de dados com a coleção [Errors](errors-collection-ado.md).

  - Ler a versão da implementação ADO usada com a propriedade [Version](version-property-ado.md).

  - Obter informações sobre o esquema do banco de dados com o método [OpenSchema](openschema-method-ado.md).

Crie os objetos **Connection** independentemente de qualquer outro objeto definido anteriormente.

Execute os comandos ou procedimentos armazenados como se fossem métodos nativos no objeto **Connection**, como exemplificado a seguir.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Executar um comando como um método nativo de um objeto Connection

Para executar um comando, forneça o nome dele usando o objeto **Command** da propriedade [Name](name-property-ado.md). Defina a propriedade **ActiveConnection** do objeto **Command** para a conexão. Em seguida, emita uma instrução na qual o nome do comando será usado como se fosse um método do objeto **Connection**, seguido por quaisquer parâmetros e depois por um objeto **Recordset** se quaisquer linhas forem retornadas. Defina as propriedades **Recordset** para personalizar o **Recordset** resultante. Por exemplo:

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Executar um procedimento armazenado com um método nativo do objeto Connection

Para executar um procedimento armazenado, emita uma instrução na qual o nome do procedimento armazenado seja usado como se fosse um método do objeto **Connection**, seguido por quaisquer parâmetros. O ADO se tornará a "melhor solução" dos tipos de parâmetros. Por exemplo:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
