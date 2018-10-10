---
title: Caixa de diálogo de propriedades personalizadas do controle ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463969"
---
# <a name="activex-controls-custom-properties-dialog-box"></a><span data-ttu-id="9118c-102">Caixa de diálogo de propriedades personalizadas do controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="9118c-102">ActiveX Control's Custom Properties Dialog Box</span></span>

<span data-ttu-id="9118c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9118c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9118c-p101">Durante a definição das propriedades de um controle ActiveX, pode ser que você precise ou prefira utilizar a caixa de diálogo de propriedades personalizadas do controle. Essa caixa de diálogo de propriedades personalizadas oferece uma alternativa à lista de propriedades da folha de propriedades do Microsoft Access para definir as propriedades dos controles ActiveX no modo de design.</span><span class="sxs-lookup"><span data-stu-id="9118c-p101">When setting the properties of an ActiveX control, you may need or prefer to use the control's custom properties dialog box. This custom properties dialog box provides an alternative to the list of properties in the Microsoft Access property sheet for setting ActiveX control properties in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="9118c-106">[!OBSERVAçãO] Essas informações somente se aplicam aos controles ActiveX em um ambiente de banco de dados do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9118c-106">This information only applies to ActiveX controls in a Microsoft Access database environment.</span></span>



## <a name="two-ways-to-set-properties"></a><span data-ttu-id="9118c-107">Duas maneiras de definir propriedades</span><span class="sxs-lookup"><span data-stu-id="9118c-107">Two Ways to Set Properties</span></span>

<span data-ttu-id="9118c-p102">A razão pela qual existe a caixa de diálogo de propriedades personalizadas é que nem todos os aplicativos que utilizam os controles ActiveX proporcionam uma folha de propriedades como aquela do Microsoft Access. A caixa de diálogo de propriedades personalizadas oferece uma interface para a definição das propriedades de controles-chave, independentemente da interface oferecida pelo aplicativo hospedeiro.</span><span class="sxs-lookup"><span data-stu-id="9118c-p102">The reason for the custom properties dialog box is that not all applications that use ActiveX controls provide a property sheet like the one in Microsoft Access. The custom properties dialog box provides an interface for setting key control properties regardless of the interface supplied by the hosting application.</span></span>

<span data-ttu-id="9118c-110">Para algumas propriedades de controles ActiveX, você pode optar por uma destas duas localizações para definir a propriedade:</span><span class="sxs-lookup"><span data-stu-id="9118c-110">For some ActiveX control properties, you can choose either of these two locations to set the property:</span></span>

  - <span data-ttu-id="9118c-111">A folha de propriedades do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9118c-111">The Microsoft Access property sheet.</span></span>

  - <span data-ttu-id="9118c-112">A caixa de diálogo de propriedades personalizadas do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9118c-112">The ActiveX control's custom properties dialog box.</span></span>

<span data-ttu-id="9118c-p103">Em alguns casos, a caixa de diálogo de propriedades personalizadas é a única maneira de definir uma propriedade no modo de design. Isto geralmente ocorre quando a interface precisa definir uma propriedade que não funciona dentro da folha de propriedades do Microsoft Access. Por exemplo, a propriedade **GridFont** para o Controle de Calendário tem muitos argumentos; você não pode definir mais de um argumento por propriedade na folha de propriedades do Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="9118c-p103">In some cases, the custom properties dialog box is the only way to set a property in Design view. This is usually the situation when the interface needed to set a property doesn't work inside the Microsoft Access property sheet. For example, the **GridFont** property for the Calendar control has a number of arguments; you can't set more than one argument per property in the Microsoft Access property sheet.</span></span>

## <a name="finding-the-custom-properties-dialog-box"></a><span data-ttu-id="9118c-116">Localizando a caixa de diálogo de propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="9118c-116">Finding the Custom Properties Dialog Box</span></span>

<span data-ttu-id="9118c-p104">Nem todos os controles ActiveX proporcionam uma caixa de diálogo de propriedades personalizadas. Para ver se um controle oferece essa caixa de diálogo de propriedades personalizadas, procure pela propriedade **Personalizar** na folha de propriedades do Microsoft Access para esse controle. Se a lista de propriedades contiver o nome **Personalizar**, então o controle oferece a caixa de diálogo de propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="9118c-p104">Not all ActiveX controls provide a custom properties dialog box. To see whether a control provides this custom properties dialog box, look for the **Custom** property in the Microsoft Access property sheet for this control. If the list of properties contains the name **Custom**, then the control provides the custom properties dialog box.</span></span>

## <a name="using-the-custom-properties-dialog-box"></a><span data-ttu-id="9118c-120">Utilizando a caixa de diálogo de propriedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="9118c-120">Using the Custom Properties Dialog Box</span></span>

<span data-ttu-id="9118c-p105">Depois de clicar na caixa da propriedade **Personalizar** na folha de propriedades do Microsoft Access, clique no botão **Construir** à direita da caixa de propriedades para exibir a caixa de diálogo de propriedades personalizadas do controle, apresentada frequentemente como uma caixa de diálogo com guias. Escolha a guia que contém a interface para a configuração das propriedades que você deseja definir.</span><span class="sxs-lookup"><span data-stu-id="9118c-p105">After you click the **Custom** property box in the Microsoft Access property sheet, click the **Build** button to the right of the property box to display the control's custom properties dialog box, often presented as a tabbed dialog box. Choose the tab that contains the interface for setting the properties that you want to set.</span></span>

<span data-ttu-id="9118c-p106">Após fazer as alterações em uma guia, em geral, é possível aplicar essas alterações clicando imediatamente no botão **Aplicar** (se fornecido). Você pode clicar em outras guias para definir outras propriedades, se necessário. Para aprovar todas as alterações feitas na caixa de diálogo de propriedades personalizadas, clique no botão **OK**. Para retornar à folha de propriedades do Microsoft Access sem alterar nenhuma definição de propriedade, clique no botão **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="9118c-p106">After you make changes on one tab, you can often apply those changes immediately by clicking the **Apply** button (if provided). You can click other tabs to set other properties as needed. To approve all changes made in the custom properties dialog box, click the **OK** button. To return to the Microsoft Access property sheet without changing any property settings, click the **Cancel** button.</span></span>

<span data-ttu-id="9118c-p107">Você também pode visualizar a caixa de diálogo de propriedades personalizadas clicando no subcomando **Propriedades** do comando **Objeto** do controle ActiveX (por exemplo, **Objeto Calendar Control**) no menu **Editar**, ou clicando nesse mesmo subcomando no menu de atalho do controle ActiveX. Além disso, algumas propriedades na folha de propriedades do Microsoft Access para o controle ActiveX, como a propriedade **GridFontColor** do Controle de Calendário, têm um botão **Construir** à direita da caixa de propriedades. Quando você clica no botão **Construir**, a caixa de diálogo de propriedades personalizadas é exibida, com a guia apropriada selecionada (por exemplo, **Cores**).</span><span class="sxs-lookup"><span data-stu-id="9118c-p107">You can also view the custom properties dialog box by clicking the **Properties** subcommand of the ActiveX control **Object** command (for example, **Calendar Control Object**) on the **Edit** menu, or by clicking this same subcommand on the shortcut menu for the ActiveX control. In addition, some properties in the Microsoft Access property sheet for the ActiveX control, like the **GridFontColor** property of the Calendar control, have a **Build** button to the right of the property box. When you click the **Build** button, the custom properties dialog box is displayed, with the appropriate tab selected (for example, **Colors**).</span></span>

