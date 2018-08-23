---
title: IMAPIStatusSettingsDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.SettingsDialog
api_type:
- COM
ms.assetid: e931246e-7fff-4116-a9fc-f685988e21e8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a21feb474ef69da9ec8e36e06c8649b9d0f93981
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566702"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="0aa57-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="0aa57-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="0aa57-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa57-105">Exibe uma folha de propriedades que permite ao usuário alterar a configuração de um provedor de serviços, que esse método não é suportado nos objetos de status que implementa de MAPI.</span><span class="sxs-lookup"><span data-stu-id="0aa57-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0aa57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0aa57-106">Parameters</span></span>

 <span data-ttu-id="0aa57-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0aa57-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0aa57-108">[in] Uma alça para a janela pai da folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="0aa57-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="0aa57-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0aa57-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0aa57-110">[in] Uma bitmask dos sinalizadores que controla a exibição da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0aa57-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="0aa57-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="0aa57-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0aa57-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="0aa57-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="0aa57-113">Sugere que o provedor não deve habilitar os usuários alterem as propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="0aa57-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="0aa57-114">Esse sinalizador é apenas uma sugestão; pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="0aa57-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0aa57-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0aa57-115">Return value</span></span>

<span data-ttu-id="0aa57-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0aa57-116">S_OK</span></span> 
  
> <span data-ttu-id="0aa57-117">A folha de propriedades de configuração foi exibida com êxito.</span><span class="sxs-lookup"><span data-stu-id="0aa57-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="0aa57-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0aa57-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0aa57-119">O objeto status não suporta este método, conforme indicado pela ausência do sinalizador STATUS_SETTINGS_DIALOG na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0aa57-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0aa57-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0aa57-120">Remarks</span></span>

<span data-ttu-id="0aa57-121">O método **IMAPIStatus:: SettingsDialog** exibe uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="0aa57-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="0aa57-122">Todos os provedores de serviço devem oferecer suporte para o método **SettingsDialog** , mas ela não é necessária.</span><span class="sxs-lookup"><span data-stu-id="0aa57-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="0aa57-123">Provedores de serviço podem implementar suas próprias folhas de propriedade ou use a implementação fornecida no método de [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) de suporte do objeto.</span><span class="sxs-lookup"><span data-stu-id="0aa57-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="0aa57-124">**DoConfigPropsheet** constrói uma folha de propriedades de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0aa57-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0aa57-125">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="0aa57-125">Notes to implementers</span></span>

<span data-ttu-id="0aa57-126">Se um provedor de transporte remoto tiver quaisquer configurações, ele deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0aa57-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="0aa57-127">Abra a seção de perfil do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0aa57-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="0aa57-128">Obtenha o transporte configurações de propriedade do provedor do perfil.</span><span class="sxs-lookup"><span data-stu-id="0aa57-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="0aa57-129">Exiba as configurações de propriedade em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0aa57-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="0aa57-130">Se a caixa de diálogo permite a edição das configurações de propriedade, verifique se as novas configurações são válidas e armazená-los novamente na seção de perfil do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="0aa57-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="0aa57-131">Retorne S_OK ou quaisquer valores de erro retornados durante as etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="0aa57-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="0aa57-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0aa57-132">Notes to callers</span></span>

<span data-ttu-id="0aa57-133">Você pode usar a folha de propriedades exibida por meio de **SettingsDialog** para realizar várias tarefas, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0aa57-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="0aa57-134">Especifique um armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="0aa57-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="0aa57-135">Especifica uma ordem de transporte.</span><span class="sxs-lookup"><span data-stu-id="0aa57-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="0aa57-136">Especifique um contêiner de catálogo de endereços padrão para navegação.</span><span class="sxs-lookup"><span data-stu-id="0aa57-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="0aa57-137">Especifica uma ordem de pesquisa para resolução de nomes ambíguos.</span><span class="sxs-lookup"><span data-stu-id="0aa57-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="0aa57-138">Especifique um catálogo de endereços pessoal padrão.</span><span class="sxs-lookup"><span data-stu-id="0aa57-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="0aa57-139">Provedores de serviço podem implementar folhas de propriedades que são de leitura/gravação, somente leitura, ou uma mistura de permissões, dependendo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0aa57-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="0aa57-140">Provedores de serviços podem implementar diferentes permissões nas propriedades individuais, definindo restrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0aa57-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="0aa57-141">O modo padrão de folhas de propriedade é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0aa57-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="0aa57-142">Você pode solicitar folhas de propriedade somente leitura, definindo o sinalizador UI_READONLY em suas chamadas a **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="0aa57-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="0aa57-143">Provedores de serviço podem implementar folhas de propriedade somente leitura podem fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="0aa57-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="0aa57-144">No entanto, pois alguns provedores de serviços não podem substituir o modo padrão, você deve ser preparado para lidar com as folhas de propriedades de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="0aa57-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="0aa57-145">Como uma interface de usuário é sempre envolvida nesta operação, somente clientes interativos devem chamar **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="0aa57-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0aa57-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="0aa57-146">See also</span></span>



[<span data-ttu-id="0aa57-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="0aa57-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="0aa57-148">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="0aa57-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="0aa57-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0aa57-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

