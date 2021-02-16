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
# <a name="imapistatussettingsdialog"></a><span data-ttu-id="72538-103">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="72538-103">IMAPIStatus::SettingsDialog</span></span>

  
  
<span data-ttu-id="72538-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72538-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72538-105">Exibe uma folha de propriedades que permite ao usuário alterar a configuração de um provedor de serviços Esse método não é suportado em objetos de status que o MAPI implementa.</span><span class="sxs-lookup"><span data-stu-id="72538-105">Displays a property sheet that enables the user to change a service provider's configuration This method is not supported in status objects that MAPI implements.</span></span>
  
```cpp
HRESULT SettingsDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="72538-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72538-106">Parameters</span></span>

 <span data-ttu-id="72538-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="72538-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="72538-108">[in] Um alça para a janela pai da folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="72538-108">[in] A handle to the parent window of the configuration property sheet.</span></span>
    
 <span data-ttu-id="72538-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72538-109">_ulFlags_</span></span>
  
> <span data-ttu-id="72538-110">[in] Uma máscara de bits de sinalizadores que controla a exibição da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="72538-110">[in] A bitmask of flags that controls the display of the property sheet.</span></span> <span data-ttu-id="72538-111">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="72538-111">The following flag can be set:</span></span>
    
<span data-ttu-id="72538-112">UI_READONLY</span><span class="sxs-lookup"><span data-stu-id="72538-112">UI_READONLY</span></span> 
  
> <span data-ttu-id="72538-113">Sugere que o provedor não deve permitir que os usuários alterem as propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="72538-113">Suggests that the provider should not enable users to change configuration properties.</span></span> <span data-ttu-id="72538-114">Esse sinalizador é apenas uma sugestão; ela pode ser ignorada.</span><span class="sxs-lookup"><span data-stu-id="72538-114">This flag is only a suggestion; it can be ignored.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72538-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="72538-115">Return value</span></span>

<span data-ttu-id="72538-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="72538-116">S_OK</span></span> 
  
> <span data-ttu-id="72538-117">A folha de propriedades de configuração foi exibida com êxito.</span><span class="sxs-lookup"><span data-stu-id="72538-117">The configuration property sheet was displayed successfully.</span></span>
    
<span data-ttu-id="72538-118">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="72538-118">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="72538-119">O objeto de status não dá suporte a esse método, conforme indicado pela ausência do sinalizador STATUS_SETTINGS_DIALOG na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="72538-119">The status object does not support this method, as indicated by the absence of the STATUS_SETTINGS_DIALOG flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72538-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="72538-120">Remarks</span></span>

<span data-ttu-id="72538-121">O **método IMAPIStatus::SettingsDialog** exibe uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="72538-121">The **IMAPIStatus::SettingsDialog** method displays a configuration property sheet.</span></span> <span data-ttu-id="72538-122">Todos os provedores de serviços devem dar suporte **ao método SettingsDialog,** mas isso não é necessário.</span><span class="sxs-lookup"><span data-stu-id="72538-122">All service providers should support the **SettingsDialog** method, but it is not required.</span></span> <span data-ttu-id="72538-123">Os provedores de serviços podem implementar suas próprias folhas de propriedades ou usar a implementação fornecida no [método IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) do objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="72538-123">Service providers can implement their own property sheets or use the implementation supplied in the support object's [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method.</span></span> <span data-ttu-id="72538-124">**DoConfigPropsheet** cria uma folha de propriedades de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="72538-124">**DoConfigPropsheet** builds a read/write property sheet.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="72538-125">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="72538-125">Notes to implementers</span></span>

<span data-ttu-id="72538-126">Se um provedor de transporte remoto tiver configurações, ele deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="72538-126">If a remote transport provider has any settings, it should do the following:</span></span>
  
- <span data-ttu-id="72538-127">Abra a seção de perfil do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="72538-127">Open the transport provider's profile section.</span></span>
    
- <span data-ttu-id="72538-128">Obter as configurações de propriedade do provedor de transporte do perfil.</span><span class="sxs-lookup"><span data-stu-id="72538-128">Get the transport provider's property settings from the profile.</span></span>
    
- <span data-ttu-id="72538-129">Exibe as configurações de propriedade em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="72538-129">Display the property settings in a dialog box.</span></span>
    
- <span data-ttu-id="72538-130">Se a caixa de diálogo permitir a edição das configurações de propriedade, verifique se as novas configurações são válidas e armazene-as novamente na seção de perfil do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="72538-130">If the dialog box allows editing of the property settings, check that the new settings are valid and store them back in the transport provider's profile section.</span></span>
    
- <span data-ttu-id="72538-131">Retornar S_OK ou qualquer valor de erro retornado durante as etapas anteriores.</span><span class="sxs-lookup"><span data-stu-id="72538-131">Return S_OK, or any error values returned during the preceding steps.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="72538-132">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="72538-132">Notes to callers</span></span>

<span data-ttu-id="72538-133">Você pode usar a folha de propriedades exibida por **meio de SettingsDialog** para executar várias tarefas, como as seguintes:</span><span class="sxs-lookup"><span data-stu-id="72538-133">You can use the property sheet displayed through **SettingsDialog** to perform a variety of tasks, such as the following:</span></span> 
  
- <span data-ttu-id="72538-134">Especifique um armazenamento de mensagens padrão.</span><span class="sxs-lookup"><span data-stu-id="72538-134">Specify a default message store.</span></span>
    
- <span data-ttu-id="72538-135">Especifique um pedido de transporte.</span><span class="sxs-lookup"><span data-stu-id="72538-135">Specify a transport order.</span></span>
    
- <span data-ttu-id="72538-136">Especifique um contêiner de agendamento de endereço padrão para navegação.</span><span class="sxs-lookup"><span data-stu-id="72538-136">Specify a default address book container for browsing.</span></span>
    
- <span data-ttu-id="72538-137">Especifique uma ordem de pesquisa para resolver nomes ambíguos.</span><span class="sxs-lookup"><span data-stu-id="72538-137">Specify a search order for resolving ambiguous names.</span></span>
    
- <span data-ttu-id="72538-138">Especifique um livro de endereços pessoal padrão.</span><span class="sxs-lookup"><span data-stu-id="72538-138">Specify a default personal address book.</span></span>
    
<span data-ttu-id="72538-139">Os provedores de serviços podem implementar folhas de propriedades de leitura/gravação, somente leitura ou uma combinação de permissões, dependendo da propriedade.</span><span class="sxs-lookup"><span data-stu-id="72538-139">Service providers can implement property sheets that are read/write, read-only, or a mixture of permissions, depending on the property.</span></span> <span data-ttu-id="72538-140">Os provedores de serviços podem implementar permissões diferentes em propriedades individuais definindo restrições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="72538-140">Service providers can implement different permissions on individual properties by setting property restrictions.</span></span> <span data-ttu-id="72538-141">O modo padrão para folhas de propriedades é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="72538-141">The default mode for property sheets is read/write.</span></span> <span data-ttu-id="72538-142">Você pode solicitar folhas de propriedades somente leitura definindo o sinalizador UI_READONLY em suas chamadas para **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="72538-142">You can request read-only property sheets by setting the UI_READONLY flag in your calls to **SettingsDialog**.</span></span> <span data-ttu-id="72538-143">Os provedores de serviços que são capazes de implementar folhas de propriedades somente leitura podem fazer isso.</span><span class="sxs-lookup"><span data-stu-id="72538-143">Service providers that are able to implement read-only property sheets can do so.</span></span> <span data-ttu-id="72538-144">No entanto, como alguns provedores de serviços não podem substituir o modo padrão, você deve estar preparado para lidar com folhas de propriedade de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="72538-144">However, because some service providers cannot override the default mode, you must be prepared to handle property sheets of either type.</span></span> 
  
<span data-ttu-id="72538-145">Como uma interface do usuário está sempre envolvida nessa operação, somente clientes interativos devem chamar **SettingsDialog**.</span><span class="sxs-lookup"><span data-stu-id="72538-145">Because a user interface is always involved in this operation, only interactive clients should call **SettingsDialog**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72538-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="72538-146">See also</span></span>



[<span data-ttu-id="72538-147">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="72538-147">IMAPISupport::DoConfigPropsheet</span></span>](imapisupport-doconfigpropsheet.md)
  
[<span data-ttu-id="72538-148">Propriedade canônica PidTagResourceMethods</span><span class="sxs-lookup"><span data-stu-id="72538-148">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
  
[<span data-ttu-id="72538-149">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="72538-149">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

