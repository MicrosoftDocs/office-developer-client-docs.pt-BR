---
title: Criar um controle ActiveX que pode associar-se a dados de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Você pode hospedar os Controles ActiveX nos formulários do InfoPath que podem ser abertos no InfoPath editor. Esses controles podem preexistentes (com algumas restrições) ou podem ser escritos especificamente para InfoPath.
ms.openlocfilehash: 70ac6a16b305403ffa99d8fe840a165913642f57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300186"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="c8da2-104">Criar um controle ActiveX que pode associar-se a dados de formulário do InfoPath</span><span class="sxs-lookup"><span data-stu-id="c8da2-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="c8da2-105">Você pode hospedar os Controles ActiveX nos formulários do InfoPath que podem ser abertos no InfoPath editor.</span><span class="sxs-lookup"><span data-stu-id="c8da2-105">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor.</span></span> <span data-ttu-id="c8da2-106">Esses controles podem preexistentes (com algumas restrições) ou podem ser escritos especificamente para InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c8da2-106">These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="c8da2-107">Escrever um controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="c8da2-107">Write an ActiveX Control</span></span>

<span data-ttu-id="c8da2-108">Como com outros controles no InfoPath, os controles ActiveX devem suportar interfaces de modelo COM (Component Object) existente:</span><span class="sxs-lookup"><span data-stu-id="c8da2-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="c8da2-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c8da2-109">**IDispatch**</span></span>
    
- <span data-ttu-id="c8da2-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="c8da2-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="c8da2-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="c8da2-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="c8da2-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="c8da2-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="c8da2-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="c8da2-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="c8da2-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="c8da2-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="c8da2-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="c8da2-115">**IViewObject**</span></span>
    
- <span data-ttu-id="c8da2-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="c8da2-116">**IOleObject**</span></span>
    
- <span data-ttu-id="c8da2-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="c8da2-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="c8da2-118">Para que o InfoPath atualize propriedades no modelo de objeto de documento (DOM) no momento em que alterar no controle, o controle deve implementar o interfaces seguintes:</span><span class="sxs-lookup"><span data-stu-id="c8da2-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="c8da2-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="c8da2-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="c8da2-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="c8da2-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="c8da2-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="c8da2-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="c8da2-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="c8da2-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="c8da2-123">Além disso, há duas interfaces específicas do InfoPath COM que fornecem uma integração maior de controles:</span><span class="sxs-lookup"><span data-stu-id="c8da2-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="c8da2-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="c8da2-124">IInfoPathControl</span></span>](https://msdn.microsoft.com/library/bb264625.aspx)
    
- [<span data-ttu-id="c8da2-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="c8da2-125">IInfoPathControlSite</span></span>](https://msdn.microsoft.com/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="c8da2-126">Adicionar um controle ActiveX para o ambiente de Design do InfoPath</span><span class="sxs-lookup"><span data-stu-id="c8da2-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="c8da2-127">O comando**adicionar ou remover controles personalizados** no **painel de tarefas** controles permite que você use o **Assistente para adicionar controle personalizado** para adicionar um controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="c8da2-127">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control.</span></span> <span data-ttu-id="c8da2-128">Usando o assistente, você pode selecionar um controle ActiveX que já foi registrado ou localizar mais controles personalizados no Marketplace do Office.</span><span class="sxs-lookup"><span data-stu-id="c8da2-128">By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace.</span></span> <span data-ttu-id="c8da2-129">Depois de selecionar um controle, você pode especificar os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8da2-129">After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="c8da2-130">Especifique um gabinete para instalar o controle ActiveX com seu modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="c8da2-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="c8da2-131">Especifica uma propriedade de associação para associar ao XML.</span><span class="sxs-lookup"><span data-stu-id="c8da2-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="c8da2-132">Especifique uma propriedade usada para ativar ou desativar o controle em resposta às regras ou assinaturas digitais, que podem ser úteis, por exemplo, quando não houver XML ou quando a formatação condicional é usada.</span><span class="sxs-lookup"><span data-stu-id="c8da2-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="c8da2-133">Para especificar dados digite encadernação.</span><span class="sxs-lookup"><span data-stu-id="c8da2-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="c8da2-134">Se você estiver desenvolvendo um controle ActiveX e adicioná-lo para o **painel de tarefas** controles no InfoPath, não será possível recriar o controle ActiveX até InfoPath é fechado.</span><span class="sxs-lookup"><span data-stu-id="c8da2-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="c8da2-135">Implantar um controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="c8da2-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="c8da2-136">Para distribuir um controle ActiveX, você pode gravar uma instalação que instala o controle no computador de destino e copia o arquivo de modelo de controle do InfoPath (TIC) e o arquivo de gabinete para a pasta do usuário, \Users\\< nome de usuário\>\AppData\ Local\Microsoft\InfoPath\Controls.</span><span class="sxs-lookup"><span data-stu-id="c8da2-136">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls.</span></span> <span data-ttu-id="c8da2-137">Observe que, se dois ou mais desenvolvedores de duas ou estiverem colaborando no desenvolvimento de formulários com controles ActiveX, cada desenvolvedor deve ter os controles que foram adicionados para o ambiente de design InfoPath ou não será possível modificar as propriedades dos controles de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="c8da2-137">Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c8da2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8da2-138">See also</span></span>

<span data-ttu-id="c8da2-139">Laboratório 6: Adicionar controles ActiveX no InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="c8da2-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="c8da2-140">Criar um controle de personalizado InfoPath utilizando c# e .NET (Blog da equipe InfoPath)</span><span class="sxs-lookup"><span data-stu-id="c8da2-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](https://blogs.msdn.microsoft.com/infopath/2005/04/15/creating-an-infopath-custom-control-using-c-and-net/)

