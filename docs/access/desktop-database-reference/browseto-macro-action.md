---
title: Ação de macro ProcurarEm
TOCTitle: BrowseTo Macro Action
ms:assetid: b25e1cc6-c4ed-abd6-0285-94fc7dae0bdf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822020(v=office.15)
ms:contentKeyID: 48547167
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm35083
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15009ca039d5df06bc732f4b58c066ad8f8d67c9
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603760"
---
# <a name="browseto-macro-action"></a><span data-ttu-id="08b82-102">Ação de macro ProcurarEm</span><span class="sxs-lookup"><span data-stu-id="08b82-102">BrowseTo Macro Action</span></span>

<span data-ttu-id="08b82-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="08b82-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="08b82-p101">Você pode usar a ação **ProcurarEm** para navegar entre objetos no local. Também é possível alterar o objeto de origem em um controle de subformulário, especificando o argumento Caminho para Controle de Subformulário. Use **ProcurarEm** para navegar do formulário1 para o formulário1 sem precisar abrir uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="08b82-p101">You can use the **BrowseTo** action to navigate between objects in place. You can also change the source object of a subform control by specifying the Path to Subform Control argument. Use **BrowseTo** to navigate from form1 to form2 without opening up a new window.</span></span>

## <a name="setting"></a><span data-ttu-id="08b82-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="08b82-107">Setting</span></span>

<span data-ttu-id="08b82-108">A ação **ProcurarEm** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="08b82-108">The **BrowseTo** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="08b82-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="08b82-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="08b82-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="08b82-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="08b82-111">Tipo de Objeto</span><span class="sxs-lookup"><span data-stu-id="08b82-111">Object Type</span></span></p></td>
<td><p><span data-ttu-id="08b82-112">O tipo de objeto que será procurado.</span><span class="sxs-lookup"><span data-stu-id="08b82-112">The object type to which to browse.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08b82-113">Nome do Objeto</span><span class="sxs-lookup"><span data-stu-id="08b82-113">Object Name</span></span></p></td>
<td><p><span data-ttu-id="08b82-114">O objeto que carrega o controle de subformulário referenciado pelo argumento Caminho para Controle de Subformulário.</span><span class="sxs-lookup"><span data-stu-id="08b82-114">The object that loads inside the subform control referenced by the Path to Subform Control argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08b82-115">Caminho para Controle de Subformulário</span><span class="sxs-lookup"><span data-stu-id="08b82-115">Path to Subform Control</span></span></p></td>
<td><p><span data-ttu-id="08b82-116">Se especificado, o caminho do formulário principal do aplicativo para o subformulário de destino de controle que carrega o objeto especificado pelo argumento Nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="08b82-116">If specified, the path from the main form of the application to the target subform control that loads the object specified by the Object Name argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08b82-117">Condição Where</span><span class="sxs-lookup"><span data-stu-id="08b82-117">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="08b82-118">Se estiver especificado, substitui a condição Where da fonte de registro de objeto.</span><span class="sxs-lookup"><span data-stu-id="08b82-118">If specified, replaces the Where condition of the object record source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="08b82-119">Page</span><span class="sxs-lookup"><span data-stu-id="08b82-119">Page</span></span></p></td>
<span data-ttu-id="08b82-120"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="08b82-120"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="08b82-p102">Se estiver especificado, define a página do formulário contínuo que se tornará a página atual. Esse argumento é somente da Web.</span><span class="sxs-lookup"><span data-stu-id="08b82-p102">If specified, sets the page of the continuous form that will be made the current page. This argument is Web only.</span></span></p></td>
=======
<td><p><span data-ttu-id="08b82-123">Se estiver especificado, define a página do formulário contínuo que se tornará a página atual.</span><span class="sxs-lookup"><span data-stu-id="08b82-123">If specified, sets the page of the continuous form that will be made the current page.</span></span> <span data-ttu-id="08b82-124">Esse argumento será apenas web.</span><span class="sxs-lookup"><span data-stu-id="08b82-124">This argument is web only.</span></span></p></td><span data-ttu-id="08b82-125">
>>>>>>>mestre</span><span class="sxs-lookup"><span data-stu-id="08b82-125">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="08b82-126">Modo de Dados</span><span class="sxs-lookup"><span data-stu-id="08b82-126">Data Mode</span></span></p></td>
<td><p><span data-ttu-id="08b82-127">Se for especificado, o modo de entrada de dados do formulário.</span><span class="sxs-lookup"><span data-stu-id="08b82-127">If specified, the data entry mode of the form.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="08b82-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="08b82-128">Remarks</span></span>

<span data-ttu-id="08b82-129">O argumento CaminhoparaControledeSubformulário deve ser especificado por meio do uso da sintaxe do seguinte exemplo de código:</span><span class="sxs-lookup"><span data-stu-id="08b82-129">The PathToSubFormControl argument must be specified using the syntax in the following code example:</span></span>

```vb
    Main Form.SubForm Ctrl 1>Form 2.SubForm Ctrl 2>Form 3.SubFormCtrl3
```

<span data-ttu-id="08b82-p104">Neste exemplo, o Formulário principal é o formulário de nível superior no aplicativo cliente do Access. O argumento Caminho para Controle de Subformulário deve especificar, alternadamente, os nomes de formulário e de subformulário desde o formulário principal até o controle de subformulário que é o contêiner do objeto especificado pelo argumento Nome de Objeto. Cada controle de subformulário especificado deve ser um controle do formulário que o precede. O caminho deve terminar com um controle de subformulário.</span><span class="sxs-lookup"><span data-stu-id="08b82-p104">In this example, the Main Form is the top level form in the Access client application. The Path to Sub Form Control argument must alternately specify form and subform control names leading from the main form to the subform control that is the container of the object specified by the Object Name argument. Each subform control specified must be a control on the form that precedes it. The path must end with a subform control.</span></span>

## <a name="example"></a><span data-ttu-id="08b82-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="08b82-134">Example</span></span>

<span data-ttu-id="08b82-135">O exemplo a seguir mostra como usar a ação procurarem para abrir um relatório em um controle subformulário ou dentro de um controle de navegação.</span><span class="sxs-lookup"><span data-stu-id="08b82-135">The following example shows how to use the BrowseTo action to open a report in a subform control or within a navigation control.</span></span>

<span data-ttu-id="08b82-136">**Código de exemplo fornecido pela** [referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="08b82-136">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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



