---
title: Coleção Errors (DAO)
TOCTitle: Errors Collection
ms:assetid: d42007b5-6410-14e9-baf9-9306fdef38f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834805(v=office.15)
ms:contentKeyID: 48547929
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7f118bab1a73d29858776e33149c54aab39ef5cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462306"
---
# <a name="errors-collection-dao"></a>Coleção Errors (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Uma coleção **Errors** contém todos os objetos **Error** armazenados, cada um dos quais pertence a uma única operação envolvendo o DAO.

## <a name="remarks"></a>Comentários

Qualquer operação envolvendo objetos do DAO pode gerar um ou mais erros. Quando cada erro ocorre, um ou mais objetos **Error** são colocados na coleção **Errors** do objeto **DBEngine**. Quando outra operação do DAO gera um erro, a coleção **Errors** é limpa e o novo conjunto de objetos **Error** é colocado na coleção **Errors**. O objeto de número mais elevado na coleção **Errors **(DBEngine.Errors.Count - 1) corresponde ao erro informado pelo objeto **Err** do Microsoft Visual Basic for Applications (VBA).

Operações do DAO que não geram erro não produzem efeito na coleção **Errors**.

Elementos da coleção **Errors** não são acrescentados como geralmente ocorre com outras coleções, portanto a coleção **Errors** não oferece suporte para os métodos **Append** e **Delete**.

O conjunto de objetos **Error** na coleção **Errors** descreve um erro. O primeiro objeto **Error** é o erro de nível mais baixo, o segundo, o próximo nível mais alto, e assim por diante. Por exemplo, se um erro de ODBC ocorre durante a tentativa de abrir um objeto **[Recordset](recordset-object-dao.md)**, o primeiro objeto error contém o erro de ODBC de nível mais baixo; erros subsequentes contêm os erros de ODBC retornados pelas várias camadas de ODBC. Neste caso, o gerenciador de driver ODBC e possivelmente o próprio driver retornam objetos **Error** separados. O último objeto **Error** contém o erro do DAO indicando que o objeto não pôde ser aberto.

Enumerar os erros específicos na coleção **Errors** permite que suas rotinas de manipulação de erros determinem mais precisamente a causa e a origem de um erro e tomem as medidas de recuperação apropriadas.


> [!NOTE]
> <P>[!OBSERVAçãO] Se você utiliza a palavra-chave <STRONG>New</STRONG> para criar um objeto que causa um erro tanto antes como quando ele está sendo colocado na coleção <STRONG>Errors</STRONG>, a coleção não conterá informações de erro sobre aquele objeto, porque o novo objeto não está associado ao objeto <STRONG>DBEngine</STRONG>. No entanto, a informação de erro estará disponível no objeto <STRONG>Err</STRONG> do VBA.</P>



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

