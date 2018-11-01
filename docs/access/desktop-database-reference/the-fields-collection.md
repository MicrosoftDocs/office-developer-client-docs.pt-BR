---
title: A coleção Fields
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67f16c9c4dd27fdbd57a2c082580ead0606298e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874871"
---
# <a name="the-fields-collection"></a>A coleção Fields


**Aplica-se a**: Access 2013, o Office 2013

A coleção **Fields** é uma das coleções intrínsecas do ADO. Uma coleção é um conjunto ordenado de itens ao qual podemos nos referir como uma unidade.

A coleção **Fields** contém um objeto **Field** para cada campo (coluna) no **Recordset**. Como todas as coleções do ADO, ela possui as propriedades **Count** e **Item**, além dos métodos **Append** e **Refresh**. Ela também possui métodos **CancelUpdate**, **Delete**, **Resync** e **Update**, que não estão disponíveis para outras coleções da ADO.

## <a name="examining-the-fields-collection"></a>Examinando a coleção Fields

Considere a coleção **Fields** do **Recordset** de exemplo apresentado neste capítulo. O **Recordset** de exemplo foi derivado da instrução SQL

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Assim, você descobrirá que a coleção **Fields** do **Recordset** contém três campos.

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

Esse código determina simplesmente o número de objetos **Field** na coleção **Fields** usando a propriedade **Count** e os loops pela coleção, retornando o valor da propriedade **Name** de cada objeto **Field**. Você pode usar muitas outras propriedades de **Field** para obter informações sobre um campo. Para obter mais informações sobre como consultar um **campo**, consulte [O objeto Field](the-field-object.md).

## <a name="counting-columns"></a>Contando colunas

Como você deve esperar, a propriedade **Count** retorna o número real de objetos **Field** na coleção **Fields**. Como a numeração dos participantes de uma coleção começa com zero, você sempre deve codificar os loops começando com o participante zero e terminado com o valor da propriedade **Count** menos 1. Se estiver usando o Microsoft Visual Basic e desejar fazer um loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For** **Each...Next**.

Se a propriedade **Count** for zero, não haverá objetos na coleção.

## <a name="getting-to-the-field"></a>Chegando ao Field

Como em qualquer coleção do ADO, a propriedade **Item** é a propriedade padrão da coleção. Ela retorna o objeto **Field** individual especificado pelo nome ou índice passado para ela. Portanto, as instruções a seguir são equivalentes para o **Recordset** de exemplo:

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Se esses métodos são equivalentes, qual é o melhor? Depende. Usar um índice para recuperar um **campo** da coleção é mais rápido porque ele acessa o **campo** diretamente, sem precisar executar uma busca de sequência. Por outro lado, a ordem de **campos** na coleção deve ser conhecida e, se a ordem for alterada, a referência ao índice de **campos** deverá ser alterado, onde quer que ocorra. Apesar de um pouco mais lenta, a utilização do nome do **campo** é mais flexível porque não depende da ordem dos **campos** na coleção.

## <a name="using-the-refresh-method"></a>Usando o método Refresh

Diferente de algumas outras coleções do ADO, a utilização do método **Refresh** na coleção **Fields** não tem nenhum efeito visível. Para recuperar alterações da estrutura do banco de dados de base, você deve usar o método **Requery** ou, se o objeto **Recordset** não oferecer suporte a indicadores, o método **MoveFirst**, que fará o comando ser executado contra o provedor novamente.

## <a name="adding-fields-to-a-recordset"></a>Adicionando campos a um Recordset

O método **Append** é usado para adicionar campos a um **Recordset**.

Você pode usar o método **Append** para fabricar um **Recordset** por programação, sem abrir uma conexão com uma origem de dados. Ocorrerá um erro em tempo de execução se o método **Append** for chamado na coleção **Fields** de um **Recordset** aberto ou em um **Recordset** onde a propriedade **ActiveConnection** tiver sido definida. Você pode acrescentar campos apenas a um **Recordset** que não esteja aberto e ainda não esteja conectado a uma origem de dados. Contudo, para especificar valores para os **campos** recém-acrescentados, o **Recordset** deverá ser aberto primeiro.

Frequentemente os desenvolvedores precisam de um lugar para armazenar alguns dados temporariamente ou desejam que alguns dados atuem como se viessem de um servidor de forma que possam participar na ligação de dados em uma interface do usuário. O ADO (em conjunto com o [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) permite que o desenvolvedor crie um objeto **Recordset** vazio especificando informações de coluna e chamando **Open**. No exemplo a seguir, três novos campos são acrescentados a um objeto **Recordset** novo. Em seguida, o **Recordset** é aberto, dois registros novos são adicionados e o **Recordset** é mantido em um arquivo. (Para obter mais informações sobre a manutenção do **Recordset**, consulte o [Capítulo 5: Atualizando e mantendo dados](chapter-5-updating-and-persisting-data.md).)

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

O uso do método **Append** dos **campos** difere entre o objeto **Recordset** e o objeto **Record**. Para obter mais informações sobre o objeto **Record**, consulte o [Capítulo 10: Registros e fluxos](chapter-10-records-and-streams.md).

