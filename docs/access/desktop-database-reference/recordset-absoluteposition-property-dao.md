---
title: Propriedade Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300697"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Propriedade Recordset.AbsolutePosition (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna o número de registro relativo do registro atual de um objeto **Recordset**.

## <a name="syntax"></a>Sintaxe

*expressão* .AbsolutePosition

*expressão* Uma variável que representa um objeto **Recordset**.

## <a name="remarks"></a>Comentários

Você pode usar a propriedade **AbsolutePosition** para posicionar o ponteiro do registro atual para um registro específico baseado na sua posição ordinal, em um objeto **Recordset** tipo dynaset ou instantâneo. Você também pode determinar o número atual do registro, verificando a configuração da propriedade **AbsolutePosition**.

Como o valor da propriedade **AbsolutePosition** é zero (isto é, uma configuração de 0 se refere aos primeiro registro no objeto **Recordset**), você não pode defini-lo como um valor maior ou igual ao número de registros preenchidos; fazer isso pode causar um erro interceptável. Você pode determinar o número de registros preenchidos no objeto **Recordset**, verificando a configuração da propriedade **RecordCount**. A configuração máxima permitida para a propriedade **AbsolutePosition** é o valor da propriedade **RecordCount** menos 1.

Se não houver registro atual, assim como nenhum registro no objeto **Recordset**, **AbsolutePosition** retorna – 1. Caso o registro atual seja excluído, o valor da propriedade **AbsolutePosition** não será definido e ocorrerá um erro interceptável se for mencionado. Novos registros são adicionados ao final da sequência.

Você não deve usar essa propriedade como um número de registro substituto. Os indicadores ainda são a forma recomendada de reter e retornar a uma determinada posição e são a única maneira de posicionar o registro atual em todos os tipos de objetos **Recordset**. Em particular, a posição de um registro é alterada quando um ou mais registros anteriores a ele são excluídos. Também não há nenhuma garantia de que um registro terá a mesma posição absoluta se o objeto **Recordset** for recriado, pois a ordem de registros individuais dentro de um objeto **Recordset** não é garantida, a menos que ela seja criada com uma instrução SQL, utilizando uma cláusula ORDER BY.

> [!NOTE]
> - Definir a propriedade **AbsolutePosition** para um valor maior que zero em um objeto **Recordset** recém-aberto, mas não preenchido, causa um erro interceptável. Preencha o objeto **Recordset** primeiro com o método **MoveLast**.
> - A propriedade **AbsolutePosition** não está disponível nos objetos **Recordset** do tipo somente encaminhamento ou nos objetos **Recordset** abertos em consultas de passagem nos bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **AbsolutePosition** para controlar o progresso de um loop que enumera todos os registros de um **Recordset**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
