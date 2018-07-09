---
title: Criar um controle ActiveX que pode vincular dados de formulário do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a0d62047-bf08-9f70-de00-7f81ef1331f1
description: Você pode hospedar controles ActiveX em formulários do InfoPath que foram projetados para ser aberto no editor do InfoPath. Esses controles podem ser preexistente (com algumas restrições) ou podem ser escritos especificamente para o InfoPath.
ms.openlocfilehash: 90378533a7c3cde4a1927753c0325fdd8d0b3ce5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765594"
---
# <a name="create-an-activex-control-that-can-bind-to-infopath-form-data"></a><span data-ttu-id="0b3d9-104">Criar um controle ActiveX que pode vincular dados de formulário do InfoPath</span><span class="sxs-lookup"><span data-stu-id="0b3d9-104">Create an ActiveX Control that can Bind to InfoPath Form Data</span></span>

<span data-ttu-id="0b3d9-105">Você pode hospedar controles ActiveX em formulários do InfoPath que foram projetados para ser aberto no editor do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-105">You can host ActiveX controls in InfoPath forms that are designed to be opened in the InfoPath editor.</span></span> <span data-ttu-id="0b3d9-106">Esses controles podem ser preexistente (com algumas restrições) ou podem ser escritos especificamente para o InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-106">These controls can be preexisting (with some constraints) or can be written specifically for InfoPath.</span></span>
  
## <a name="write-an-activex-control"></a><span data-ttu-id="0b3d9-107">Escrever um controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="0b3d9-107">Write an ActiveX Control</span></span>

<span data-ttu-id="0b3d9-108">Assim como acontece com outros controles no InfoPath, os controles ActiveX devem oferecer suporte a interfaces existentes do objeto COM (Component Model):</span><span class="sxs-lookup"><span data-stu-id="0b3d9-108">As with other controls in InfoPath, ActiveX controls should support existing Component Object Model (COM) interfaces:</span></span>
  
- <span data-ttu-id="0b3d9-109">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-109">**IDispatch**</span></span>
    
- <span data-ttu-id="0b3d9-110">**IPersistPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-110">**IPersistPropertyBag**</span></span>
    
- <span data-ttu-id="0b3d9-111">**IPersistStreamInit**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-111">**IPersistStreamInit**</span></span>
    
- <span data-ttu-id="0b3d9-112">**IPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-112">**IPropertyPage**</span></span>
    
- <span data-ttu-id="0b3d9-113">**IObjectSafety**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-113">**IObjectSafety**</span></span>
    
- <span data-ttu-id="0b3d9-114">**IPropertyNotifySink**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-114">**IPropertyNotifySink**</span></span>
    
- <span data-ttu-id="0b3d9-115">**IViewObject**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-115">**IViewObject**</span></span>
    
- <span data-ttu-id="0b3d9-116">**IOleObject**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-116">**IOleObject**</span></span>
    
- <span data-ttu-id="0b3d9-117">**IOleInPlaceObject**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-117">**IOleInPlaceObject**</span></span>
    
<span data-ttu-id="0b3d9-118">Na ordem do InfoPath atualizar as propriedades no documento DOM (Object Model) no momento em que eles alterar no controle, o controle deve implementar estas interfaces:</span><span class="sxs-lookup"><span data-stu-id="0b3d9-118">In order for InfoPath to update properties in the Document Object Model (DOM) at the time that they change in the control, the control should implement the following interfaces:</span></span>
  
- <span data-ttu-id="0b3d9-119">**IConnectionPointContainer**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-119">**IConnectionPointContainer**</span></span>
    
- <span data-ttu-id="0b3d9-120">**IEnumConnectionPoints**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-120">**IEnumConnectionPoints**</span></span>
    
- <span data-ttu-id="0b3d9-121">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-121">**IConnectionPoint**</span></span>
    
- <span data-ttu-id="0b3d9-122">**IEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-122">**IEnumConnections**</span></span>
    
<span data-ttu-id="0b3d9-123">Além disso, há duas interfaces COM InfoPath específica que oferecem maior integração dos controles:</span><span class="sxs-lookup"><span data-stu-id="0b3d9-123">Also, there are two InfoPath-specific COM interfaces that provide tighter integration of controls:</span></span>
  
- [<span data-ttu-id="0b3d9-124">IInfoPathControl</span><span class="sxs-lookup"><span data-stu-id="0b3d9-124">IInfoPathControl</span></span>](http://msdn.microsoft.com/pt-br/library/bb264625.aspx)
    
- [<span data-ttu-id="0b3d9-125">IInfoPathControlSite</span><span class="sxs-lookup"><span data-stu-id="0b3d9-125">IInfoPathControlSite</span></span>](http://msdn.microsoft.com/pt-br/library/bb264627.aspx)
    
## <a name="add-an-activex-control-to-the-infopath-design-environment"></a><span data-ttu-id="0b3d9-126">Adicionar um controle ActiveX para o ambiente de Design do InfoPath</span><span class="sxs-lookup"><span data-stu-id="0b3d9-126">Add an ActiveX Control to the InfoPath Design Environment</span></span>

<span data-ttu-id="0b3d9-127">O comando **Adicionar ou remover controles personalizados** no painel de tarefas **controles** permite que você use o **Assistente para adicionar personalizado controle** para adicionar um controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-127">The **Add or Remove Custom Controls** command on the **Controls** task pane enables you to use the **Add Custom Control Wizard** to add a custom control.</span></span> <span data-ttu-id="0b3d9-128">Usando o assistente, você pode selecionar um controle ActiveX que já foi registrado ou localizar controles personalizados adicionais no Office Marketplace.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-128">By using the wizard, you can select an ActiveX control that has already been registered or find additional custom controls on Office Marketplace.</span></span> <span data-ttu-id="0b3d9-129">Depois de selecionar um controle, você pode especificar os itens a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-129">After you select a control, you can specify the following items.</span></span> 
  
- <span data-ttu-id="0b3d9-130">Especifique um arquivo CAB para instalar o controle ActiveX com o seu modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-130">Specify a CAB to install the ActiveX control with your form template.</span></span>
    
- <span data-ttu-id="0b3d9-131">Especifique uma propriedade de vinculação para vincular ao XML.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-131">Specify a binding property to bind to the XML.</span></span>
    
- <span data-ttu-id="0b3d9-132">Especifique uma propriedade que é usada para habilitar ou desabilitar o controle em resposta às regras ou assinaturas digitais, que podem ser útil, por exemplo, quando o XML não estiver presente ou quando a formatação condicional é usada.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-132">Specify a property that is used to enable or disable the control in response to rules or digital signatures, which can be useful, for example, when the XML is not present or when conditional formatting is used.</span></span>
    
- <span data-ttu-id="0b3d9-133">Especificar dados digite ligação.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-133">Specify data type binding.</span></span>
    
> [!NOTE]
> <span data-ttu-id="0b3d9-134">Se você estiver desenvolvendo um controle ActiveX e adicionou ao painel de tarefas **controles** no InfoPath, não será possível reconstruir o controle ActiveX até InfoPath é fechado.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-134">If you are developing an ActiveX control and have added it to the **Controls** task pane in InfoPath, you will be unable to rebuild the ActiveX control until InfoPath is closed.</span></span> 
  
## <a name="deploy-an-activex-control"></a><span data-ttu-id="0b3d9-135">Implantar um controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="0b3d9-135">Deploy an ActiveX Control</span></span>

<span data-ttu-id="0b3d9-136">Para distribuir um controle ActiveX, você pode escrever um instalador que instala o controle no computador de destino e copia o arquivo de modelo de controle do InfoPath (ICT) e o arquivo CAB para a pasta do usuário, \Users\\< username\>\AppData\Local\ Microsoft\InfoPath\Controls.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-136">To distribute an ActiveX control, you can write an installer that installs the control on the target computer and copies the InfoPath Control Template (ICT) file and the CAB file to the user's folder, \Users\\<username\>\AppData\Local\Microsoft\InfoPath\Controls.</span></span> <span data-ttu-id="0b3d9-137">Observe que se dois ou mais desenvolvedores estão colaborando sobre como desenvolver formulários que usam os controles ActiveX, cada desenvolvedor deve ter os controles que foram adicionados ao ambiente de design do InfoPath ou não será possível modificar as propriedades dos controles do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-137">Note that if two or more developers are collaborating on developing forms that use ActiveX controls, each developer should have the controls that were added to the InfoPath design environment, or they will be unable to modify the properties of the controls from InfoPath.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0b3d9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b3d9-138">See also</span></span>



<span data-ttu-id="0b3d9-139">Laboratório 6: Adicionando controles ActiveX no InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="0b3d9-139">Lab 6: Adding ActiveX Controls in InfoPath 2003</span></span>
  
[<span data-ttu-id="0b3d9-140">Criar um controle personalizado do InfoPath usando c# e .NET (Blog da equipe do InfoPath)</span><span class="sxs-lookup"><span data-stu-id="0b3d9-140">Creating an InfoPath Custom Control using C# and .NET (InfoPath Team Blog)</span></span>](http://blogs.msdn.com/infopath/archive/2005/04/15/creating-an-infopath-custom-control-using-c-and-net.aspx)

