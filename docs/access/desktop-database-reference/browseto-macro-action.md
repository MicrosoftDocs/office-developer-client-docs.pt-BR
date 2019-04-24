---
title: Ação da macro ProcurarEm
TOCTitle: BrowseTo macro action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bcf0a37f8c1596856f5d7b921430371d620f7a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296770"
---
# <a name="browseto-macro-action"></a>Ação da macro ProcurarEm

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **ProcurarEm** para navegar entre objetos no local. Também é possível alterar o objeto de origem em um controle de subformulário, especificando o argumento Caminho para Controle de Subformulário. Use **ProcurarEm** para navegar do formulário1 para o formulário1 sem precisar abrir uma nova janela.

## <a name="setting"></a>Configuração

A ação **ProcurarEm** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Tipo de Objeto</p></td>
<td><p>O tipo de objeto até o qual você deseja navegar.</p></td>
</tr>
<tr class="even">
<td><p>Nome do Objeto</p></td>
<td><p>O objeto que carrega o controle de subformulário referenciado pelo argumento Caminho para Controle de Subformulário.</p></td>
</tr>
<tr class="odd">
<td><p>Caminho para Controle de Subformulário</p></td>
<td><p>Se especificado, o caminho do formulário principal do aplicativo para o controle de subformulário de destino que carrega o objeto especificado pelo argumento Nome do objeto.</p></td>
</tr>
<tr class="even">
<td><p>Condição Where</p></td>
<td><p>Se for especificado, substitui a condição Where da origem de registro do objeto.</p></td>
</tr>
<tr class="odd">
<td><p>Page</p></td>
<td><p>Se estiver especificado, define a página do formulário contínuo que se tornará a página atual. Este argumento é somente Web.</p></td>
</tr>
<tr class="even">
<td><p>Modo de Dados</p></td>
<td><p>Se for especificado, o modo de entrada de dados do formulário.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

O argumento CaminhoparaControledeSubformulário deve ser especificado por meio do uso da sintaxe do seguinte exemplo de código:

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

Neste exemplo, o Formulário principal é o formulário de nível superior no aplicativo cliente do Access. O argumento Caminho para Controle de Subformulário deve especificar, alternadamente, os nomes de formulário e de subformulário desde o formulário principal até o controle de subformulário que é o contêiner do objeto especificado pelo argumento Nome de Objeto. Cada controle de subformulário especificado deve ser um controle do formulário que o precede. O caminho deve terminar com um controle de subformulário.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação procurarem para abrir um relatório em um controle de subformulário ou dentro de um controle de navegação.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    OnError
        Go to Next
        Macro Name
    
    /* Try to load the report in the host form (frmAuthorsParameter)    */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
    
    /* if this fails, try to load it in the navigation subform     */
    BrowseTo
        Object Type Report
        Object Name rptChapters
        Path to Subform Control frmMain.NavigationSubform>frmAuthorsParameter.sfrmChild
        Where Condition
        Page
        Data Mode Edit
    
    Parameters
        SelectedAuthor =[cboAuthor]
```



