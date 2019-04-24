---
title: Atuar como um provedor de catálogo de endereços de host
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331266"
---
# <a name="acting-as-a-host-address-book-provider"></a>Atuar como um provedor de catálogo de endereços de host

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de host é um provedor de catálogo de endereços que inclui destinatários de outros provedores em seus contêineres e depende da implementação dos destinatários por outros provedores para controlar parcialmente sua manutenção. Um provedor de host usa os identificadores de modelo desses destinatários estrangeiros para vincular os dados desses destinatários ao código no provedor estrangeiro. Esse processo de associação é iniciado quando o provedor recupera a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) de um destinatário e a transmite em uma chamada para [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). 
  
Quando o provedor chama **IMAPISupport:: OpenTemplateID**, MAPI corresponde ao **MAPIUID** dentro do identificador de modelo com um **MAPIUID** registrado por um provedor e chama o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) do provedor. O provedor estrangeiro pode retornar um ponteiro para o objeto Property do provedor, à sua própria implementação de objeto Property ou a uma implementação que envolve o objeto do provedor. O ponteiro retornado é colocado no conteúdo do parâmetro _lppMAPIPropNew_ . 
  
Seu provedor pode escolher se deseja ou não chamar **IMAPISupport:: OpenTemplateID** com o sinalizador FILL_ENTRY definido. Defina esse sinalizador quando o destinatário estiver sendo criado ou quando um longo tempo decorrido desde que seu provedor tenha atualizado as propriedades do destinatário. Um uso comum do sinalizador FILL_ENTRY é manter um destinatário no seu provedor sincronizado com o original. A implementação desse tipo de agendamento de sincronização melhora o desempenho. 
  
 **Para manter um destinatário estrangeiro sincronizado**
  
1. Determine um intervalo apropriado para atualizações periódicas. 
    
2. Cada chamada de carimbo de data/hora para [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Avaliar se é necessário ou não a execução de uma atualização completa com base na quantidade de tempo que expirou desde a última chamada. Se uma atualização completa for necessária, chame **IMAPISupport:: OpenTemplateID** com o sinalizador FILL_ENTRY. Se não for necessário, não defina o sinalizador na chamada. 
    
Quando um cliente faz uma solicitação para uma das propriedades do destinatário copiado, seu provedor pode escolher se deseja lidar com a solicitação ou usar o código fornecido pelo provedor estrangeiro. Seu provedor pode esperar que o provedor estrangeiro intercepte a maioria, se não todos, as chamadas para **IMAPIProp** , exceto [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Uma chamada para **OpenProperty** solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) é sempre encaminhada para seu provedor.
  
 **Para acessar o código de identificador de modelo**
  
1. Abra o destinatário e chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps para recuperar a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Se **** GetProps falhar porque o **PR_TEMPLATEID** não está disponível, o provedor estrangeiro não oferece suporte a um identificador de modelo e código relacionado para esse destinatário. Seu provedor precisará usar sua implementação do destinatário para todas as manutenções. 
    
2. Se o identificador de modelo é retornado **** de GetProps, passe-o e um ponteiro para a implementação do **IMAPIProp** do destinatário em uma chamada para o método **IMAPISupport:: OpenTemplateID** . Defina o sinalizador FILL_ENTRY se a maioria ou todas as propriedades do destinatário precisam ser atualizadas, como no momento da criação ou se elas não foram atualizadas por um tempo. 
    
3. Se **OpenTemplateID** retornar a implementação de **IMAPIProp** do provedor estrangeiro, retorne ao cliente um ponteiro para esta implementação. 
    
4. Se o **OpenTemplateID** não retornar uma implementação, normalmente porque o provedor estrangeiro não está no perfil, retorne ao cliente um ponteiro para a implementação do **IMAPIProp** do provedor. O cliente deve ser capaz de trabalhar com as propriedades do objeto usando qualquer uma das interfaces. 
    

