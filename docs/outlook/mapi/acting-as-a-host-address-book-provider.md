---
title: Atuando como um provedor de lista de endereços de host
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406462"
---
# <a name="acting-as-a-host-address-book-provider"></a>Atuando como um provedor de lista de endereços de host

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de host é um provedor de agendas que inclui destinatários de outros provedores em seus contêineres e depende da implementação dos destinatários pelos outros provedores para controlar parcialmente sua manutenção. Um provedor de host usa os identificadores de modelo desses destinatários externos para vincular os dados desses destinatários ao código no provedor estrangeiro. Esse processo de associação é iniciado quando seu provedor recupera a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de um destinatário e a passa em uma chamada para [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
  
Quando seu provedor chama **IMAPISupport::OpenTemplateID**, MAPI corresponde ao **MAPIUID** no identificador de modelo com um **MAPIUID** registrado por um provedor e chama o método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) do provedor. O provedor externo pode retornar um ponteiro para o objeto de propriedade do provedor, para sua própria implementação de objeto de propriedade ou para uma implementação que quebra o objeto do provedor. O ponteiro retornado é colocado no conteúdo do _parâmetro lppMAPIPropNew._ 
  
Seu provedor pode optar por chamar **IMAPISupport::OpenTemplateID** com o sinalizador FILL_ENTRY definido. De definir esse sinalizador quando o destinatário estiver sendo criado ou quando já tiver passado muito tempo desde que o provedor atualize as propriedades do destinatário. Um uso comum do sinalizador FILL_ENTRY é manter um destinatário em seu provedor sincronizado com o original. Implementar esse tipo de agendamento de sincronização melhora o desempenho. 
  
 **Para manter um destinatário estrangeiro sincronizado**
  
1. Determine um intervalo apropriado para atualizações periódicas. 
    
2. Timestamp cada chamada para [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Avalie se é necessário ou não executar uma atualização completa com base na quantidade de tempo que expirou desde a última chamada. Se uma atualização completa for necessária, chame **IMAPISupport::OpenTemplateID** com o sinalizador FILL_ENTRY dados. Se não for necessário, não de definir o sinalizador na chamada. 
    
Quando um cliente faz uma solicitação para uma das propriedades do destinatário copiado, seu provedor pode optar por manipular a solicitação em si ou usar o código fornecido pelo provedor estrangeiro. Seu provedor pode esperar que o provedor estrangeiro intercepte a maioria das chamadas para **IMAPIProp,** se não todas, exceto [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Uma chamada para **OpenProperty** solicitando a **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) é sempre encaminhada para seu provedor.
  
 **Para acessar o código do identificador do modelo**
  
1. Abra o destinatário e chame seu método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar a **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) . Se **o GetProps** falhar **PR_TEMPLATEID** não estiver disponível, o provedor externo não dá suporte a um identificador de modelo e código relacionado para esse destinatário. Seu provedor precisará usar a implementação do destinatário para toda a manutenção. 
    
2. Se o identificador do modelo for retornado de **GetProps**, passe-o e um ponteiro para a implementação **IMAPIProp** do destinatário em uma chamada para o método **IMAPISupport::OpenTemplateID.** De definida FILL_ENTRY sinalizador se a maioria ou todas as propriedades do destinatário precisam ser atualizadas, como no momento da criação ou se elas não foram atualizadas por algum tempo. 
    
3. Se **OpenTemplateID** retornar a implementação **IMAPIProp** do provedor estrangeiro, retorne ao cliente um ponteiro para essa implementação. 
    
4. Se **OpenTemplateID** não retornar uma implementação, normalmente porque o provedor estrangeiro não está no perfil, retorne ao cliente um ponteiro para a implementação **IMAPIProp** do provedor. O cliente deve ser capaz de trabalhar com as propriedades do objeto usando qualquer uma das interfaces. 
    

