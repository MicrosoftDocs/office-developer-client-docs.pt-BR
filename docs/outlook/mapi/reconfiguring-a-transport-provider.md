---
title: Reconfigurando um provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408405"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="27df3-103">Reconfigurando um provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="27df3-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="27df3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27df3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27df3-105">Você pode usar o objeto de status de um provedor de transporte para alterar algumas das propriedades do provedor.</span><span class="sxs-lookup"><span data-stu-id="27df3-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="27df3-106">O intervalo de propriedades que podem ser alteradas depende das propriedades incluídas na folha de propriedades do provedor e de como essas propriedades são definidas.</span><span class="sxs-lookup"><span data-stu-id="27df3-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="27df3-107">**Para reconfigurar um provedor de transporte ativo**</span><span class="sxs-lookup"><span data-stu-id="27df3-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="27df3-108">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="27df3-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="27df3-109">Localize a linha para o provedor de transporte a ser reconfigurado criando uma restrição de propriedade que corresponde PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) com o nome do provedor de destino.</span><span class="sxs-lookup"><span data-stu-id="27df3-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="27df3-110">Chame [IMAPITable::FindRow](imapitable-findrow.md) para recuperar a linha apropriada.</span><span class="sxs-lookup"><span data-stu-id="27df3-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="27df3-111">Verifique se os sinalizadores STATUS_SETTINGS_DIALOG e STATUS_VALIDATE_STATE estão definidos na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do provedor de transporte de destino.</span><span class="sxs-lookup"><span data-stu-id="27df3-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="27df3-112">Se STATUS_SETTINGS_DIALOG não estiver definida, o provedor de transporte não exibirá uma folha de propriedades de configuração.</span><span class="sxs-lookup"><span data-stu-id="27df3-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="27df3-113">Se STATUS_VALIDATE_STATE não estiver definido, não será possível executar a reconfiguração dinâmica.</span><span class="sxs-lookup"><span data-stu-id="27df3-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="27df3-114">Se STATUS_SETTINGS_DIALOG estiver definido, chame [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para exibir a folha de propriedades do provedor de transporte e permitir que o usuário faça alterações.</span><span class="sxs-lookup"><span data-stu-id="27df3-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="27df3-115">Depois que o usuário terminar a reconfiguração, chame [IMAPIStatus::ValidateState](imapistatus-validatestate.md) se STATUS_VALIDATE_STATE estiver definido, passando CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="27df3-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

