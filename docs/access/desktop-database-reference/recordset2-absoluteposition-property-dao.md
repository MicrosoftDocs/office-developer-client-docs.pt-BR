---
title: Propriedade Recordset2.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4de869866e2aeb28032553be78bee7af16f60402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307508"
---
# <a name="recordset2absoluteposition-property-dao"></a>Propriedade Recordset2.AbsolutePosition (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna o número de registros relativos de um registro atual do objeto **Recordset2**.

## <a name="syntax"></a>Sintaxe

*expressão* .AbsolutePosition

*expressão* Uma variável que representa **um objeto Recordset2** .

## <a name="remarks"></a>Comentários

Você pode usar a propriedade **AbsolutePosition** para posicionar o ponteiro do registro atual em um registro específico com base em sua posição ordinal em um objeto **Recordset2** do tipo dynaset ou instantâneo. Também será necessário determinar o número de registros atual pela verificação da definição da propriedade **AbsolutePosition**.

Como o valor da propriedade **AbsolutePosition** está baseado em zero (ou seja, uma definição de 0 refere-se ao primeiro registro do objeto **Recordset2**), não será possível definir um valor maior ou igual ao número de registros preenchidos, pois isso ocasionará um erro interceptável. Determine o número de registros preenchidos no objeto **Recordset2** por meio da verificação da definição da propriedade **RecordCount**. A definição máxima permitida da propriedade **AbsolutePosition** é o valor da propriedade **RecordCount** menos 1.

Se não houver nenhum registro atual, como quando não há registros no objeto **Recordset2,** **AbsolutePosition** retornará –1. Caso o registro atual seja excluído, o valor da propriedade **AbsolutePosition** não será definido e ocorrerá um erro interceptável se for mencionado. Novos registros são adicionados ao final da sequência.

Você não deverá usar essa propriedade como um número de registro substituto. Os indicadores ainda são a forma recomendada de retenção e de retorno de uma determinada posição e são a única forma de posicionamento do registro atual em todos os tipos de objetos **Recordset2**. Em especial, a posição de um registro será alterada quando um ou vários registros precedentes forem excluídos. Também não existirá nenhuma garantia de que um registro terá a mesma posição absoluta, se o objeto **Recordset2** recriado novamente devido à ordem dos registros individuais em um objeto **Recordset** não for garantido, a não ser que seja criada com uma instrução SQL por meio da cláusula ORDER BY.

> [!NOTE]
> - A definição da propriedade **AbsolutePosition** como um valor maior que zero em um objeto **Recordset2** recentemente aberto, mas não preenchido, causará um erro interceptável. Preencha primeiro o objeto **Recordset2** com o método **MoveLast**.
> - A propriedade **AbsolutePosition** não está disponível em objetos **Recordset2** do tipo somente encaminhamento ou em objetos **Recordset2** abertos a partir de consultas passagem em bancos de dados ODBC conectados ao mecanismo de banco de dados do Microsoft Access.

## <a name="example"></a>Exemplo

Este exemplo usa a propriedade **AbsolutePosition** para rastrear o progresso de um loop que enumera todos os registros de um **Recordset2**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
