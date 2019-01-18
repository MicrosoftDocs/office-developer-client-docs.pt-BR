---
title: Propriedade Error (DAO)
TOCTitle: Source Property
ms:assetid: 3c101cac-278e-025e-55a4-8a9d1ee7db3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192677(v=office.15)
ms:contentKeyID: 48544302
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053360
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 79c5fa1e01bbb6bce4f2cef705f23f3259bf0678
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707406"
---
# <a name="errorsource-property-dao"></a>Propriedade Error (DAO)


**Aplica-se a**: Access 2013, o Office 2013


Retorna o nome do objeto ou do aplicativo que gerou originalmente o erro.

## <a name="syntax"></a>Sintaxe

*expressão* . Fonte

*expressão* Uma variável que representa um objeto **Error** .

## <a name="remarks"></a>Comentários

Geralmente, o valor da propriedade **Source** é o nome da classe do objeto ou a ID programática. Use a propriedade **Source** para fornecer informações aos usuários, quando o código não estiver disponível para lidar com um erro gerado em um objeto em outro aplicativo.

Por exemplo, se você acessar o Microsoft Excel e ele gerar um erro de "Divisão por zero", o Microsoft Excel define **Number** para o código do Microsoft Excel para esse erro e define a propriedade **Source** como o Excel. Application. Observe que se o erro for gerado em outro objeto chamado pelo Microsoft Excel, este interceptará o erro e ainda definirá **Error.Number** como o código do Microsoft Excel. No entanto, as outras propriedades do objeto **Error** (incluindo **Source**) reterão os valores como foram definidos pelo objeto que gerou o erro. A propriedade **Source** sempre contém o nome do objeto que gerou originalmente o erro.

Com base em toda a documentação de erros, é possível gravar um código que trate o erro de forma adequada. Se houver falhas no manipulador de erros, você poderá usar as informações do objeto **[Error](error-object-dao.md)** para descrever o erro para o usuário, por meio da propriedade **Source** e das outras propriedades **Error** para fornecer ao usuário informações sobre qual objeto gerou originalmente o erro, a descrição do erro e assim por diante.


> [!NOTE]
> A construção **On Error Resume Next** poderá ser preferível a **On Error GoTo** durante a manipulação de erros gerados durante o acesso a outros objetos. A verificação da propriedade do objeto **Error** depois de cada interação com um objeto remove a ambiguidade do objeto que o código estava acessando durante a ocorrência do erro. Assim, você pode ter certeza de que o objeto colocou o código de erro em **Error.Number**, assim como aquele objeto que gerou originalmente o erro (**Error.Source**).

## <a name="example"></a>Exemplo

Este exemplo força um erro, captura-o e exibe as propriedades **Description**, **Number**, **Source**, **HelpContext** e **HelpFile** do objeto **Error** resultante.

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
