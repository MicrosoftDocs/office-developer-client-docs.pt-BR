---
title: Atuar como um provedor de catálogo de endereços de hospedagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: de0acb88eee6addc0347f5281e5fbe5070bad0a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595402"
---
# <a name="acting-as-a-host-address-book-provider"></a>Atuar como um provedor de catálogo de endereços de hospedagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de host é um provedor de catálogo de endereços que inclui os destinatários de outros provedores em seus recipientes e baseia-se na implementação dos destinatários pelos outros provedores parcialmente controlar sua manutenção. Um provedor de host usa os identificadores de modelo desses destinatários externos para associar os dados para que esses destinatários ao código no provedor estrangeiro. Esse processo de associação é iniciado quando o seu provedor recupera a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de um destinatário e o passa em uma chamada para [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
  
Quando suas chamadas de provedor **IMAPISupport::OpenTemplateID**, MAPI corresponde a **MAPIUID** dentro do identificador de modelo com um **MAPIUID** registrados por um provedor e chama o método de [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) do provedor. O provedor estrangeiro pode retornar um ponteiro para o objeto de propriedade do seu provedor, a implementação seu próprio objeto de propriedade, ou para uma implementação que distribui o objeto do seu provedor. O ponteiro retornado é colocado no conteúdo do parâmetro _lppMAPIPropNew_ . 
  
Seu provedor pode escolher se deseja ou não **IMAPISupport::OpenTemplateID** de chamada com o sinalizador FILL_ENTRY definido. Defina esse sinalizador quando o destinatário está sendo criado ou quando um longo tempo decorrido desde que o seu provedor atualizou as propriedades do destinatário. Um uso comum do sinalizador FILL_ENTRY é manter um destinatário em seu provedor sincronizado com o original. Implementar esse tipo de agenda de sincronização melhora o desempenho. 
  
 **Para manter um destinatário externo sincronizado**
  
1. Determine um intervalo apropriado para obter atualizações periódicas. 
    
2. Timestamp cada chamada para [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Avalie se ou não é necessário executar uma atualização completa com base na quantidade de tempo que expirou desde a última chamada. Se uma atualização completa for necessária, chame **IMAPISupport::OpenTemplateID** com o sinalizador FILL_ENTRY. Se não for necessário, não defina o sinalizador na chamada. 
    
Quando um cliente faz uma solicitação para uma das propriedades do destinatário copiada, seu provedor pode escolher se deseja processar a solicitação em si ou usar o código fornecido pelo provedor estrangeiro. Seu provedor pode esperar o provedor estrangeiro interceptar mais, se não todos, chamadas para **IMAPIProp** exceto [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Uma chamada para **OpenProperty** solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) sempre será encaminhada para o seu provedor.
  
 **Para acessar o código do identificador de modelo**
  
1. Abra o destinatário e chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Se **GetProps** falhar porque **PR_TEMPLATEID** não está disponível, o provedor estrangeiro não suporta um identificador de modelo e o código relacionado para o destinatário. Seu provedor precisará usar sua implementação do destinatário para todos os de manutenção. 
    
2. Se o identificador de modelo é retornado por **GetProps**, passe a ele e um ponteiro à implementação de **IMAPIProp** do destinatário em uma chamada ao método **IMAPISupport::OpenTemplateID** . Definir o sinalizador FILL_ENTRY se maioria ou todas as propriedades do destinatário precisam ser atualizado, como no momento da criação ou se eles não foram atualizados por algum tempo. 
    
3. Se **OpenTemplateID** retornar a estrangeira implementação do provedor **IMAPIProp** , volte para o cliente um ponteiro para essa implementação. 
    
4. Se **OpenTemplateID** não retorna uma implementação, geralmente porque o provedor externo não está no perfil, retorne ao cliente um ponteiro para a implementação de **IMAPIProp** do seu provedor. O cliente deve ser capaz de trabalhar com propriedades do objeto usando a interface. 
    

