---
title: Ação da macro ExibirPonteirodeAmpulheta
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 159e9f1b4cf7beab96a463ff476b4edf577e1371
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926931"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="87b68-102">Ação da macro ExibirPonteirodeAmpulheta</span><span class="sxs-lookup"><span data-stu-id="87b68-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="87b68-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="87b68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87b68-p101">Você pode usar a ação **ExibirPonteirodeAmpulheta** para alterar o ponteiro do mouse para uma imagem de ampulheta (ou outro ícone escolhido) enquanto uma macro está em execução. Esta ação pode fornecer uma indicação visual de que a macro está em execução. Isso é especialmente útil quando uma ação de macro ou a própria macro leva muito tempo para ser executada.</span><span class="sxs-lookup"><span data-stu-id="87b68-p101">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="87b68-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="87b68-107">Setting</span></span>

<span data-ttu-id="87b68-108">A ação **ExibirPonteirodeAmpulheta** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="87b68-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87b68-109">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="87b68-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="87b68-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="87b68-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87b68-111"><strong>Ampulheta Ativa</strong></span><span class="sxs-lookup"><span data-stu-id="87b68-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="87b68-p102">Clique em <strong>Sim</strong> (exibir o ícone) ou <strong>Não</strong> (exibir o ponteiro do mouse normal) na caixa <strong>Ampulheta Ativa</strong> da seção <strong>Argumentos da Ação</strong> do painel Construtor de Macros. O padrão é <strong>Sim</strong>.</span><span class="sxs-lookup"><span data-stu-id="87b68-p102">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="87b68-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="87b68-114">Remarks</span></span>

<span data-ttu-id="87b68-115">Normalmente você usa esta ação se desativou o eco usando a ação **Eco**.</span><span class="sxs-lookup"><span data-stu-id="87b68-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="87b68-116">Quando o eco está desativado, Access suspende as atualizações da tela até que a macro é concluída.</span><span class="sxs-lookup"><span data-stu-id="87b68-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="87b68-117">O Access redefine automaticamente o argumento **Ampulheta Ativa** como **Não** quando a execução da macro é concluída.</span><span class="sxs-lookup"><span data-stu-id="87b68-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="87b68-p104">No Microsoft Windows, este é o ícone definido para **Ocupado** na caixa de diálogo **Propriedades do Mouse** do Painel de Controle do Windows. O padrão para todos os sistemas operacionais Windows é um ícone de ampulheta animado.</span><span class="sxs-lookup"><span data-stu-id="87b68-p104">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel. The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="87b68-120">É possível escolher outro ícone.</span><span class="sxs-lookup"><span data-stu-id="87b68-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="87b68-121">Para executar a ação **ExibirPonteirodeAmpulheta** em um módulo do VBA (Visual Basic for Applications), use o método **Ampulheta** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="87b68-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

