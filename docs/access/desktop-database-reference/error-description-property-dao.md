---
title: Propriedade Error.Description (DAO)
TOCTitle: Description Property
ms:assetid: 47a84bec-3258-f2c7-e1af-239da39844dc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193218(v=office.15)
ms:contentKeyID: 48544601
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053358
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e261bdffb7a8cbd616515c6cbcaa7e4ea291d086
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462591"
---
# <a name="errordescription-property-dao"></a>Propriedade Error.Description (DAO)


**Aplica-se a**: Access 2013 | Office 2013
 

Retorna uma sequência descritiva associada a um erro. Essa é a propriedade padrão para o objeto **Error**.

## <a name="syntax"></a>Sintaxe

*expressão* . Descrição

*expressão* Uma variável que representa um objeto **Error** .

## <a name="remarks"></a>Comentários

A propriedade **Description** é composta por uma pequena descrição do erro. Use essa propriedade para alertar o usuário sobre um erro que você não pode ou não deseja tratar.

## <a name="example"></a>Exemplo

Este exemplo força um erro, intercepta-o e exibe as propriedades **Description**, **Number**, **Source**, **HelpContext** e **HelpFile** do objeto Error resultante.

```vb 
Sub DescriptionX() 
 
 Dim dbsTest As Database 
 
 On Error GoTo ErrorHandler 
 
 ' Intentionally trigger an error. 
 Set dbsTest = OpenDatabase("NoDatabase") 
 
 Exit Sub 
 
ErrorHandler: 
 Dim strError As String 
 Dim errLoop As Error 
 
 ' Enumerate Errors collection and display properties of 
 ' each Error object. 
 For Each errLoop In Errors 
 With errLoop 
 strError = _ 
 "Error #" & .Number & vbCr 
 strError = strError & _ 
 " " & .Description & vbCr 
 strError = strError & _ 
 " (Source: " & .Source & ")" & vbCr 
 strError = strError & _ 
 "Press F1 to see topic " & .HelpContext & vbCr 
 strError = strError & _ 
 " in the file " & .HelpFile & "." 
 End With 
 MsgBox strError 
 Next 
 
 Resume Next 
 
End Sub 
 
```

