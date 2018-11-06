---
title: Ação da macro Imprimir
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c2e5b3e2cdfb743df8a098d3978ccd3d6eb66d90
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999026"
---
# <a name="printout-macro-action"></a><span data-ttu-id="c05c6-102">Ação da macro Imprimir</span><span class="sxs-lookup"><span data-stu-id="c05c6-102">PrintOut macro action</span></span>

<span data-ttu-id="c05c6-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="c05c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c05c6-p101">Você pode usar a ação **Imprimir** para imprimir o objeto ativo no banco de dados aberto. Pode imprimir folhas de dados, relatórios, formulários, páginas de acesso a dados e módulos.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p101">You can use the **PrintOut** action to print the active object in the open database. You can print datasheets, reports, forms, data access pages, and modules.</span></span>

> [!NOTE]
> <span data-ttu-id="c05c6-106">[!OBSERVAçãO] This action will not be allowed if the database is not trusted.</span><span class="sxs-lookup"><span data-stu-id="c05c6-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="c05c6-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="c05c6-107">Setting</span></span>

<span data-ttu-id="c05c6-108">A ação **Imprimir** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="c05c6-108">The **PrintOut** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c05c6-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="c05c6-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c05c6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c05c6-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c05c6-111"><strong>Intervalo de Impressão</strong></span><span class="sxs-lookup"><span data-stu-id="c05c6-111"><strong>Print Range</strong></span></span></p></td>
<td><p><span data-ttu-id="c05c6-p102">O intervalo da impressão. Clique em <strong>Tudo</strong> (o usuário pode imprimir todo o objeto), <strong>Seleção</strong> (o usuário pode imprimir parte do objeto selecionado) ou <strong>Páginas</strong> (o usuário pode especificar um intervalo de páginas nos argumentos <strong>Da Página</strong> e <strong>À Página</strong>) na caixa <strong>Intervalo de Impressão</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Tudo</strong>.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p102">The range to print. Click <strong>All</strong> (the user can print all of the object), <strong>Selection</strong> (the user can print the part of the object that's selected), or <strong>Pages</strong> (the user can specify a range of pages in the <strong>Page From</strong> and <strong>Page To</strong> arguments) in the <strong>Print Range</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>All</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c05c6-115"><strong>Da Página</strong></span><span class="sxs-lookup"><span data-stu-id="c05c6-115"><strong>Page From</strong></span></span></p></td>
<td><p><span data-ttu-id="c05c6-p103">A primeira página que será impressa. A impressão começa na parte superior dessa página. Este argumento é obrigatório para selecionar <strong>Páginas</strong> na caixa <strong>Intervalo de Impressão</strong>.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p103">The first page to print. Printing starts at the top of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c05c6-119"><strong>À Página</strong></span><span class="sxs-lookup"><span data-stu-id="c05c6-119"><strong>Page To</strong></span></span></p></td>
<td><p><span data-ttu-id="c05c6-p104">A última página que será impressa. A impressão para na parte inferior dessa página. Este argumento é obrigatório para selecionar <strong>Páginas</strong> na caixa <strong>Intervalo de Impressão</strong>.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p104">The last page to print. Printing stops at the bottom of this page. This argument is required if you select <strong>Pages</strong> in the <strong>Print Range</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c05c6-123"><strong>Qualidade de Impressão</strong></span><span class="sxs-lookup"><span data-stu-id="c05c6-123"><strong>Print Quality</strong></span></span></p></td>
<td><p><span data-ttu-id="c05c6-p105">A qualidade de impressão. Clique em <strong>Alta</strong>, <strong>Média</strong>, <strong>Baixa</strong> ou <strong>Rascunho</strong>. Quanto menor for a qualidade, mais rapidamente o objeto será impresso. O padrão é <strong>Alta</strong>.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p105">The print quality. Click <strong>High</strong>, <strong>Medium</strong>, <strong>Low</strong>, or <strong>Draft</strong>. The lower the quality, the faster the object prints. The default is <strong>High</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c05c6-128"><strong>Copies</strong></span><span class="sxs-lookup"><span data-stu-id="c05c6-128"><strong>Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="c05c6-p106">O número de cópias que serão impressas. O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p106">The number of copies to print. The default is 1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c05c6-131"><strong>Agrupar Cópias</strong></span><span class="sxs-lookup"><span data-stu-id="c05c6-131"><strong>Collate Copies</strong></span></span></p></td>
<td><p><span data-ttu-id="c05c6-p107">Clique em <strong>Sim</strong> (agrupar as cópias impressas) ou <strong>Não</strong> (não agrupar as cópias). O objeto poderá ser impresso com mais rapidez se este argumento for definido como <strong>Não</strong>. O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p107">Click <strong>Yes</strong> (collate the printed copies) or <strong>No</strong> (do not collate copies). The object may print faster if this argument is set to <strong>No</strong>. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c05c6-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="c05c6-135">Remarks</span></span>

<span data-ttu-id="c05c6-p108">Esta ação é semelhante a selecionar um objeto, clicar na guia **Arquivo** e clicar em **Imprimir**. Com esta ação, porém, não é exibida nenhuma caixa de diálogo **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p108">This action is similar to selecting an object, clicking the **File** tab and then clicking **Print**. With this action, however, no **Print** dialog box appears.</span></span>

> [!TIP]
> <span data-ttu-id="c05c6-138">[!DICA] Se houver configurações de impressão específicas usadas com frequência, crie uma macro que contém a ação **Imprimir** com essas configurações nos argumentos.</span><span class="sxs-lookup"><span data-stu-id="c05c6-138">If you have particular print settings you use frequently, create a macro containing a **PrintOut** action with these settings in its arguments.</span></span>

<span data-ttu-id="c05c6-p109">Os argumentos desta ação correspondem às opções da caixa de diálogo **Imprimir**. Entretanto, diferentemente da ação **EncontrarRegistro** e **Localizar e Substituir**, as configurações do argumento não são compartilhadas com as opções da caixa de diálogo **Imprimir**.</span><span class="sxs-lookup"><span data-stu-id="c05c6-p109">The arguments for this action correspond to options in the **Print** dialog box. However, unlike the **FindRecord** action and **Find and Replace** dialog box, the argument settings aren't shared with the **Print** dialog box options.</span></span>

<span data-ttu-id="c05c6-141">Para executar a ação **Imprimir** em um módulo do VBA (Visual Basic for Applications), use o método **PrintOut** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="c05c6-141">To run the **PrintOut** action in a Visual Basic for Applications (VBA) module, use the **PrintOut** method of the **DoCmd** object.</span></span>

