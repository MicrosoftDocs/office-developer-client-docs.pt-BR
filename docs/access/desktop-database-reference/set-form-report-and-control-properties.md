---
title: Definir propriedades de formulário, relatório e controle
TOCTitle: Set form, report, and control properties
description: Cada formulário, relatório, seção e controle tem configurações de propriedade que você pode alterar para modificar a aparência ou o comportamento de um item específico no Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2ffb02f78bbf9d9f4c5d5b07c1ee08e3f19453b7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874599"
---
# <a name="set-form-report-and-control-properties"></a><span data-ttu-id="573ea-103">Definir propriedades de formulário, relatório e controle</span><span class="sxs-lookup"><span data-stu-id="573ea-103">Set form, report, and control properties</span></span>

<span data-ttu-id="573ea-104">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="573ea-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="573ea-p101">Cada formulário, relatório, seção e controle tem definições de propriedade que podem ser alteradas para mudar a aparência ou o comportamento daquele item em particular. Visualize e altere as propriedades utilizando a folha de propriedades, uma macro ou o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="573ea-p101">Each form, report, section, and control has property settings that you can change to alter the look or behavior of that particular item. You view and change properties by using the property sheet, macro, or Visual Basic.</span></span>

## <a name="set-properties"></a><span data-ttu-id="573ea-107">Configurar as propriedades</span><span class="sxs-lookup"><span data-stu-id="573ea-107">Set properties</span></span>

1. <span data-ttu-id="573ea-p102">No modo de design do formulário ou no modo de design do relatório, selecione o controle, seção, formulário ou relatório para o qual você deseja definir a propriedade. Você pode selecionar:</span><span class="sxs-lookup"><span data-stu-id="573ea-p102">In form Design view or report Design view, select the control, section, form, or report for which you want to set the property. You can select:</span></span>
    
   - <span data-ttu-id="573ea-110">Um ou mais controles.</span><span class="sxs-lookup"><span data-stu-id="573ea-110">One or more controls.</span></span> <span data-ttu-id="573ea-111">Para selecionar vários controles, mantenha pressionada a tecla SHIFT e escolha os controles ou arraste o ponteiro do mouse sobre os controles que você deseja selecionar.</span><span class="sxs-lookup"><span data-stu-id="573ea-111">To select multiple controls, hold down the SHIFT key and choose the controls, or drag the mouse pointer over the controls you wish to select.</span></span> <span data-ttu-id="573ea-112">Se você selecionar vários controles, a folha de propriedades exibirá somente aquelas propriedades que os controles selecionados têm em comum.</span><span class="sxs-lookup"><span data-stu-id="573ea-112">If you select multiple controls, the property sheet will display only those properties that the selected controls have in common.</span></span>
    
   - <span data-ttu-id="573ea-113">Uma seção.</span><span class="sxs-lookup"><span data-stu-id="573ea-113">One section.</span></span> <span data-ttu-id="573ea-114">Escolha o seletor de seção da seção que você deseja selecionar.</span><span class="sxs-lookup"><span data-stu-id="573ea-114">Choose the section selector of the section you wish to select.</span></span>
    
   - <span data-ttu-id="573ea-115">O formulário ou relatório inteiro.</span><span class="sxs-lookup"><span data-stu-id="573ea-115">The entire form or report.</span></span> <span data-ttu-id="573ea-116">Escolha o seletor de formulário ou relatório no canto superior esquerdo do formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="573ea-116">Choose the form selector or report selector in the upper-left corner of the form or report.</span></span>

2. <span data-ttu-id="573ea-117">Exiba a folha de propriedade clicando no objeto ou seção e escolhendo **Propriedades** no menu de atalho ou escolhendo **Propriedades** na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="573ea-117">Display the property sheet by right-clicking the object or section and then choosing **Properties** on the shortcut menu, or by choosing **Properties** on the toolbar.</span></span>

3. <span data-ttu-id="573ea-118">Escolha a propriedade para o qual você deseja definir o valor e, em seguida, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="573ea-118">Choose the property for which you want to set the value, and then do one of the following:</span></span>
    
   - <span data-ttu-id="573ea-119">Na caixa de propriedades, digite a definição ou expressão apropriada.</span><span class="sxs-lookup"><span data-stu-id="573ea-119">In the property box, type the appropriate setting or expression.</span></span>
    
   - <span data-ttu-id="573ea-120">Se a caixa de propriedades contiver uma seta, escolha a seta e, em seguida, escolha um valor na lista.</span><span class="sxs-lookup"><span data-stu-id="573ea-120">If the property box contains an arrow, choose the arrow and then choose a value in the list.</span></span>
    
   - <span data-ttu-id="573ea-121">Se um botão **Construir** aparece à direita da caixa de propriedades, escolha-para exibir um construtor ou para exibir uma caixa de diálogo com opções de construtores.</span><span class="sxs-lookup"><span data-stu-id="573ea-121">If a **Build** button appears to the right of the property box, choose it to display a builder or to display a dialog box giving you a choice of builders.</span></span> <span data-ttu-id="573ea-122">Por exemplo, você pode utilizar o Construtor de código, o Construtor de macros ou o Construtor de consultas para definir algumas propriedades.</span><span class="sxs-lookup"><span data-stu-id="573ea-122">For example, you can use the Code Builder, Macro Builder, or Query Builder to set some properties.</span></span>

## <a name="tips"></a><span data-ttu-id="573ea-123">Dicas</span><span class="sxs-lookup"><span data-stu-id="573ea-123">Tips</span></span>

- <span data-ttu-id="573ea-124">O Microsoft Access oferece uma caixa **Zoom** para a digitação e visualização de expressões ou outras configurações longas de propriedades.</span><span class="sxs-lookup"><span data-stu-id="573ea-124">Microsoft Access provides a **Zoom** box for typing and viewing expressions or other long property settings.</span></span> <span data-ttu-id="573ea-125">Para exibir a caixa **Zoom** , escolha uma caixa de propriedade na folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="573ea-125">To display the **Zoom** box, choose a property box in the property sheet.</span></span> <span data-ttu-id="573ea-126">Pressione SHIFT + F2 ou o botão direito do mouse e escolha o **Zoom** no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="573ea-126">Press SHIFT+F2, or right-click, and then choose **Zoom** on the shortcut menu.</span></span>

- <span data-ttu-id="573ea-127">Você pode definir a propriedade **ControlSource** de alguns controles digitando a definição da propriedade no próprio controle.</span><span class="sxs-lookup"><span data-stu-id="573ea-127">You can set the **ControlSource** property for some controls by typing the property setting in the control itself.</span></span>

- <span data-ttu-id="573ea-128">Você pode alterar as configurações de propriedade padrão de um tipo de controle para que os controles criados tenham as novas configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="573ea-128">You can change the default property settings for a type of control so that future controls you create will have the new default settings.</span></span>

- <span data-ttu-id="573ea-129">As configurações de propriedade de um controle acoplado podem não corresponder às configurações semelhantes no campo da tabela ou consulta de base ao qual o controle está acoplado.</span><span class="sxs-lookup"><span data-stu-id="573ea-129">The property settings of a bound control might not match the corresponding settings in the field in the underlying table or query to which the control is bound.</span></span> <span data-ttu-id="573ea-130">Se as configurações forem diferentes, as configurações do formulário ou relatório substituirão normalmente as da tabela ou consulta.</span><span class="sxs-lookup"><span data-stu-id="573ea-130">If the settings are different, the form or report settings typically override those in the table or query.</span></span>

