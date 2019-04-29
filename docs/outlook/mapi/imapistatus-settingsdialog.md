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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1e9d390a895490f2f7445c5f1ed6e0bde3a87639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439727"
---
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="31b7e-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="31b7e-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="31b7e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31b7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31b7e-105">Exibe uma folha de propriedades que permite que o usuário altere a configuração de um provedor de serviços esse método não tem suporte nos objetos de status que o MAPI implementa.</span><span class="sxs-lookup"><span data-stu-id="31b7e-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="31b7e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31b7e-106">Parameters</span></span>

 <span data-ttu-id="31b7e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="31b7e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="31b7e-108">no Uma alça para a janela pai da folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="31b7e-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="31b7e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31b7e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="31b7e-110">no Uma bitmask de sinalizadores que controla a exibição da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="31b7e-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="31b7e-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="31b7e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="31b7e-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="31b7e-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="31b7e-113">Sugere que o provedor não deve permitir que os usuários alterem as propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="31b7e-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="31b7e-114">Este sinalizador é apenas uma sugestão; pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="31b7e-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31b7e-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="31b7e-115">Return value</span></span>

<span data-ttu-id="31b7e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="31b7e-116">S_OK</span></span> 
  
> <span data-ttu-id="31b7e-117">A folha de propriedades de configuração foi exibida com êxito.</span><span class="sxs-lookup"><span data-stu-id="31b7e-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="31b7e-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="31b7e-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="31b7e-119">O objeto status não oferece suporte a esse método, conforme indicado pela ausência do sinalizador STATUS_SETTINGS_DIALOG na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="31b7e-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31b7e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="31b7e-120">Remarks</span></span>

<span data-ttu-id="31b7e-121">O método **IMAPIStatus:: SettingsDialog** exibe uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="31b7e-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="31b7e-122">Todos os provedores de serviços devem oferecer suporte ao método **SettingsDialog** , mas não são necessários.</span><span class="sxs-lookup"><span data-stu-id="31b7e-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="31b7e-123">Os provedores de serviços podem implementar suas próprias folhas de propriedades ou usar a implementação fornecida no método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) do objeto support.</span><span class="sxs-lookup"><span data-stu-id="31b7e-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="31b7e-124">**DoConfigPropsheet** cria uma folha de propriedades de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="31b7e-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="31b7e-125">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="31b7e-125">Notes to implementers</span></span>

<span data-ttu-id="31b7e-126">Se um provedor de transporte remoto tiver configurações, deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="31b7e-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="31b7e-127">Abra a seção perfil do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="31b7e-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="31b7e-128">Obtenha as configurações de Propriedade do provedor de transporte do perfil.</span><span class="sxs-lookup"><span data-stu-id="31b7e-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="31b7e-129">Exibe as configurações de propriedade em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="31b7e-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="31b7e-130">Se a caixa de diálogo permitir a edição das configurações de propriedade, verifique se as novas configurações são válidas e armazene-as novamente na seção perfil do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="31b7e-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="31b7e-131">Retorna S_OK ou qualquer valor de erro retornado durante as etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="31b7e-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="31b7e-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="31b7e-132">Notes to callers</span></span>

<span data-ttu-id="31b7e-133">Você pode usar a folha de propriedades exibida através do **SettingsDialog** para executar várias tarefas, como as seguintes:</span><span class="sxs-lookup"><span data-stu-id="31b7e-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="31b7e-134">Especifique um repositório de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="31b7e-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="31b7e-135">Especifique uma ordem de transporte.</span><span class="sxs-lookup"><span data-stu-id="31b7e-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="31b7e-136">Especifique um contêiner de catálogo de endereços padrão para navegação.</span><span class="sxs-lookup"><span data-stu-id="31b7e-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="31b7e-137">Especifique uma ordem de pesquisa para resolver nomes ambíguos.</span><span class="sxs-lookup"><span data-stu-id="31b7e-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="31b7e-138">Especifique um catálogo de endereços pessoal padrão.</span><span class="sxs-lookup"><span data-stu-id="31b7e-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="31b7e-139">Os provedores de serviços podem implementar folhas de propriedades que são leitura/gravação, somente leitura ou uma mistura de permissões, dependendo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="31b7e-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="31b7e-140">Os provedores de serviços podem implementar diferentes permissões em propriedades individuais definindo restrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="31b7e-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="31b7e-141">O modo padrão para folhas de propriedades é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="31b7e-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="31b7e-142">Você pode solicitar folhas de propriedades somente leitura Configurando o sinalizador UI_READONLY em suas chamadas para **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="31b7e-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="31b7e-143">Provedores de serviços capazes de implementar folhas de propriedades somente leitura podem fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="31b7e-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="31b7e-144">No enTanto, como alguns provedores de serviços não podem substituir o modo padrão, você deve estar preparado para lidar com as folhas de propriedades de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="31b7e-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="31b7e-145">Como uma interface do usuário está sempre envolvida nesta operação, somente os clientes interativos devem chamar **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="31b7e-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31b7e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="31b7e-146">See also</span></span>



[<span data-ttu-id="31b7e-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="31b7e-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="31b7e-148">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="31b7e-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="31b7e-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="31b7e-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

