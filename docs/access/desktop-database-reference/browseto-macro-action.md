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
# <a name="browseto-macro-action"></a><span data-ttu-id="1a5bf-102">Ação da macro ProcurarEm</span><span class="sxs-lookup"><span data-stu-id="1a5bf-102">BrowseTo macro action</span></span>

<span data-ttu-id="1a5bf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a5bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a5bf-p101">Você pode usar a ação **ProcurarEm** para navegar entre objetos no local. Também é possível alterar o objeto de origem em um controle de subformulário, especificando o argumento Caminho para Controle de Subformulário. Use **ProcurarEm** para navegar do formulário1 para o formulário1 sem precisar abrir uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="1a5bf-107">Setting</span><span class="sxs-lookup"><span data-stu-id="1a5bf-107">Setting</span></span>

<span data-ttu-id="1a5bf-108">A ação **ProcurarEm** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a5bf-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="1a5bf-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1a5bf-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a5bf-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a5bf-111">Tipo de Objeto</span><span class="sxs-lookup"><span data-stu-id="1a5bf-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="1a5bf-112">O tipo de objeto até o qual você deseja navegar.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5bf-113">Nome do Objeto</span><span class="sxs-lookup"><span data-stu-id="1a5bf-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="1a5bf-114">O objeto que carrega o controle de subformulário referenciado pelo argumento Caminho para Controle de Subformulário.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a5bf-115">Caminho para Controle de Subformulário</span><span class="sxs-lookup"><span data-stu-id="1a5bf-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="1a5bf-116">Se especificado, o caminho do formulário principal do aplicativo para o controle de subformuidade de destino que carrega o objeto especificado pelo argumento Object Name.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5bf-117">Condição Where</span><span class="sxs-lookup"><span data-stu-id="1a5bf-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="1a5bf-118">Se for especificado, substitui a condição Where da origem de registro do objeto.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a5bf-119">Page</span><span class="sxs-lookup"><span data-stu-id="1a5bf-119">Page</span></span></p></td>
<td><p><span data-ttu-id="1a5bf-120">Se estiver especificado, define a página do formulário contínuo que se tornará a página atual.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-120">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="1a5bf-121">Esse argumento é somente da Web.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-121">This argument is web only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a5bf-122">Modo de Dados</span><span class="sxs-lookup"><span data-stu-id="1a5bf-122">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="1a5bf-123">Se for especificado, o modo de entrada de dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-123">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1a5bf-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a5bf-124">Remarks</span></span>

<span data-ttu-id="1a5bf-125">O argumento CaminhoparaControledeSubformulário deve ser especificado por meio do uso da sintaxe do seguinte exemplo de código:</span><span class="sxs-lookup"><span data-stu-id="1a5bf-125">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="1a5bf-p103">Neste exemplo, o Formulário principal é o formulário de nível superior no aplicativo cliente do Access. O argumento Caminho para Controle de Subformulário deve especificar, alternadamente, os nomes de formulário e de subformulário desde o formulário principal até o controle de subformulário que é o contêiner do objeto especificado pelo argumento Nome de Objeto. Cada controle de subformulário especificado deve ser um controle do formulário que o precede. O caminho deve terminar com um controle de subformulário.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-p103">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="1a5bf-130">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1a5bf-130">Example</span></span>

<span data-ttu-id="1a5bf-131">O exemplo a seguir mostra como usar a ação ProcurarPara para abrir um relatório em um controle de subformuidade ou em um controle de navegação.</span><span class="sxs-lookup"><span data-stu-id="1a5bf-131">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="1a5bf-132">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="1a5bf-132">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



