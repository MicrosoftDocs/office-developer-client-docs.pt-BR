---
title: Objetos de objeto Error - acesso a dados (DAO)
TOCTitle: Error Object
ms:assetid: e2608bc9-bece-9b47-4562-7a2689601f75
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835711(v=office.15)
ms:contentKeyID: 48548289
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 526498ee22bc82735eb3b98e633aa3d1b4cfb610
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864099"
---
# <a name="error-object-dao"></a>Objeto Error (DAO)


**Aplica-se a**: Access 2013 | Office 2013

O objeto **Error** contém detalhes sobre os erros de acesso aos dados, que pertencem a uma única operação envolvendo DAO.

## <a name="remarks"></a>Comentários

Qualquer operação envolvendo DAO pode gerar um ou mais erros. Por exemplo, uma chamada para um servidor ODBC pode resultar em um erro no servidor de banco de dados, no ODBC e no DAO. À medida que esse tipo de erro ocorre, um objeto **Error** é colocado na coleção **Errors** do objeto **DBEngine**. Um único evento pode resultar em vários objetos **Error** aparecendo na coleção **Errors**.

Quando uma operação DAO subsequente gera um erro, a coleção **Errors** é limpa, e um ou mais novos objetos **Error** são colocados na coleção **Errors**. As operações DAO que não geram nenhum erro não são efetivadas na coleção **Errors**.

A definição dos objetos **Error** na coleção **Errors** descreve um erro. O primeiro objeto **Error** é o erro no nível mais baixo (o erro de origem), o segundo é o erro no próximo nível mais alto e assim por diante. Por exemplo, se ocorrer um erro ODBC durante a tentativa de abrir um objeto **[Recordset](recordset-object-dao.md)**, o primeiro objeto **Error**  **Errors**(0)  conterá o erro ODBC no nível mais baixo; os erros subsequentes conterão os erros ODBC retornados por várias camadas ODBC. Nesse caso, o gerenciador do driver ODBC, e possivelmente o próprio driver, retorna objetos **Error** separados. O último objeto **Error**  **Errors.Count-** 1  contém o erro DAO que indica que o objeto não pode ser aberto.

Enumerar os erros específicos na coleção **Errors** permite que as rotinas de tratamento de erros determinem de forma mais precisa a causa e a origem de um erro e executem as etapas apropriadas para recuperação. Você pode ler as propriedades do objeto **Error** para obter detalhes específicos sobre cada erro, inclusive:

  - A propriedade **[Description](error-description-property-dao.md)**, que contém o texto do alerta de erros que será exibido na tela se o erro não for rastreado.

  - A propriedade **[Number](error-number-property-dao.md)**, que contém o valor inteiro Long da constante de erros.

  - A propriedade **[Source](error-source-property-dao.md)**, que identifica o objeto que ocasionou o erro. Isso é particularmente útil quando você tem vários objetos **Error** na coleção **Errors** seguindo uma solicitação para uma fonte de dados ODBC.

  - As propriedades **HelpFile** e **HelpContext**, que indicam o arquivo e o tópico de Ajuda apropriados do Microsoft Windows, respectivamente (se houver algum) para o erro.
    

    > [!NOTE]
    > [!OBSERVAçãO] Durante uma programação no Microsoft Visual Basic for Applications, se você usar a palavra-chave **New** para criar um objeto que, subsequentemente, causa um erro antes de o objeto ser acrescentado a uma coleção, a coleção **Errors** do objeto **DBEngine** não conterá nenhum entrada para aquele erro do objeto, porque o novo objeto não está associado ao objeto **DBEngine**. Entretanto, as informações do erro estão disponíveis no objeto **Err** do VBA. Seu código de tratamento de erro deve examinar a coleção **Errors** sempre que você antecipa um erro de acesso aos dados. Se você estiver gravando uma rotina de tratamento de erro centralizada, teste o objeto **Err** do VBA para determinar se as informações do erro na coleção **Errors** são válidas. Se a propriedade **Number** do último elemento da coleção **Errors** (DBEngine.Errors.Count - 1) e o valor da correspondência objeto **Err** , você pode usar uma série de instruções **Select Case** para identificar o erro específico do DAO ou erros que ocorreram. Se eles não forem correspondentes, use o método [Refresh](errors-refresh-method-dao.md) na coleção **Errors**.



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
            "  " & .Description & vbCr 
         strError = strError & _ 
            "  (Source: " & .Source & ")" & vbCr 
         strError = strError & _ 
            "Press F1 to see topic " & .HelpContext & vbCr 
         strError = strError & _ 
            "  in the file " & .HelpFile & "." 
      End With 
      MsgBox strError 
   Next 
 
   Resume Next 
 
End Sub 
 
```

