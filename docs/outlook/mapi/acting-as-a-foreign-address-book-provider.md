---
title: Atuar como um provedor de catálogo de endereços estrangeiro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435737"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Atuar como um provedor de catálogo de endereços estrangeiro

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor estrangeiro é um provedor de catálogo de endereços que: 
  
- Atribui identificadores de modelo para seus destinatários.
    
- O suporta o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . 
    
- Fornece código para manter destinatários que existem nos contêiners de outros provedores de catálogo de endereços conhecidos como provedores de host. Este código envolve um objeto Property, normalmente uma implementação de interface **IMAPIProp** , que envolve um objeto Property do provedor de host. 
    
Atuar como um provedor externo é uma função opcional; Nem todos os provedores precisam suportar identificadores de modelo e seus códigos relacionados. Implemente seu provedor como um provedor externo se você quiser manter o controle sobre os destinatários que os provedores de host criam usando os modelos fornecidos pelo provedor. 
  
O formato que seu provedor usa para seus identificadores de entrada também pode ser usado para seus identificadores de modelo. Os identificadores de modelo devem incluir o **MAPIUID** registrado do provedor para permitir que o MAPI vincule com êxito os destinatários aos provedores apropriados. 
  
MAPI chama o método **IABLogon:: OpenTemplateID** do provedor quando um provedor de host chama [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). O provedor de host passa o identificador de modelo do destinatário no parâmetro _lpTemplateID_ em sua chamada para **IMAPISupport:: OpenTemplateID**. O MAPI determina que o identificador de modelo pertence ao seu provedor combinando o [MAPIUID](mapiuid.md) no identificador de modelo com o **MAPIUID** que seu provedor registrou no momento do logon. Em seguida, MAPI encaminha a chamada do provedor de host para seu provedor por meio do método **IABLogon:: OpenTemplateID** . 
  
O provedor de host também passa um ponteiro para sua implementação de objeto Property para o destinatário no parâmetro _lpMAPIPropData_ , um identificador de interface no parâmetro _lpInterface_ que corresponde ao tipo de implementação de interface passado no _lpMAPIPropData_e um sinalizador opcional, FILL_ENTRY. O provedor deve retornar no parâmetro _lppMAPIPropNew_ um ponteiro para uma implementação de objeto Property do tipo especificado em _lpInterface_. O ponteiro retornado pode ser para o objeto de propriedade wrapped implementado pelo provedor ou para o objeto fornecido pelo provedor de host no _lpMAPIPropData_. Seu provedor deve retornar um ponteiro de objeto Property wrapped quando:
  
- A tabela de exibição do destinatário contém controles de caixa de listagem.
    
- O endereço de email do destinatário deve ser montado de dados em vários controles de tabela de exibição.
    
- Seus problemas de provedor exibem notificações de tabela.
    
O sinalizador FILL_ENTRY indica ao seu provedor que o provedor de host exige que todas as propriedades do destinatário sejam atualizadas. Seu provedor é necessário para atender a essa solicitação.
  
Quando um provedor de host chama o método **OpenTemplateID** do seu provedor, seu provedor pode: 
  
- Atualiza periodicamente os dados de uma entrada copiada.
    
- Mantenha uma entrada copiada sincronizada com seu original, como quando uma entrada do catálogo de endereços é copiada para o catálogo de endereços pessoal.
    
- Implementar a funcionalidade que não pode ser implementada pelo provedor de host, como preencher dinamicamente as caixas de listagem na tabela de detalhes da entrada copiada dos dados em um servidor.
    
- Controlar a interação entre as propriedades em uma entrada copiada ou modelo instanciado. Por exemplo, a computação **PR_EMAIL_ADDRESS** de outras propriedades exibidas na tabela detalhes. 
    
Os primeiros dois itens são exemplos de tarefas que não exigem que seu provedor forneça um objeto Property wrapped — uma implementação do **IMAPIProp** que se baseia na implementação do provedor de host. O provedor pode simplesmente atualizar as propriedades conforme necessário e retornar, definindo o parâmetro _lppMAPIPropNew_ para apontar para o ponteiro passado pelo provedor de host no parâmetro _lpMAPIPropData_ . 
  
As segunda duas tarefas exigem que seu provedor retorne ao provedor de host um objeto Property que quebra o objeto do provedor do host com funcionalidade adicional, como a capacidade de exibir uma folha de propriedades para a entrada. Este objeto Property será um usuário de mensagens ou uma lista de distribuição, dependendo do tipo de objeto passado pelo provedor de host no parâmetro _lpMAPIPropData_ e indicado pelo identificador de interface no parâmetro _lpInterface_ . Se o parâmetro _lpMAPIPropData_ apontar para um usuário de mensagens, o objeto de propriedade wrapped do provedor deverá ser uma implementação do **IMailUser** . Se _lpMAPIPropData_ apontar para uma lista de distribuição, deverá ser uma implementação do **IDistList** . 
  
O objeto de propriedade wrapped do provedor intercepta as chamadas de método **IMAPIProp** para executar a manipulação específica de contexto do destinatário do provedor do host — o objeto que está sendo disposto. O MAPI tem apenas um requisito para objetos de propriedade wrapped: todas as chamadas para [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) devem ser passadas para o provedor de host. A implementação do provedor pode usar a tabela retornada para interceptar as notificações da tabela de exibição ou adicionar suas próprias, se necessário. 
  
A lista a seguir inclui tarefas que normalmente são implementadas no objeto de propriedade wrapped implementado por provedores externos:
  
- Pré-processamento e valores de propriedade de pré-processamento para o destinatário do host em [IMAPIProp::](imapiprop-getprops.md)GetProps.
    
- Os detalhes de manipulação exibem controles de tabela, como botões e caixas de listagem, em **IMAPIProp:: OpenProperty**.
    
- Validar ou manipular valores de propriedade para o destinatário do host em [IMAPIProp::](imapiprop-setprops.md)SetProps.
    
- Calculando propriedades obrigatórias, como **PR_EMAIL_ADDRESS** e verificando se todas as propriedades necessárias foram definidas antes de salvar o destinatário do host no [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Para implementar o IABLogon:: OpenTemplateID
  
1. Verifique se o identificador de modelo passado com o parâmetro _lpTemplateID_ é válido e se está em um formato que seu provedor reconhece. Se não for, falhará e retornará MAPI_E_INVALID_ENTRYID. 
    
2. Criar um objeto do tipo indicado pelo identificador de modelo, um usuário de mensagens, uma lista de distribuição ou um destinatário one-off. 
    
3. Chame o método **IUnknown:: AddRef** no objeto Property do provedor de host, que é o objeto apontado pelo parâmetro _lpMAPIPropData_ . 
    
4. Se o parâmetro _ulTemplateFlags_ estiver definido como FILL_ENTRY: 
    
   1. Se o novo objeto for um usuário de mensagens ou uma lista de distribuição:
      
      1. Recupere todas as propriedades do novo objeto, possivelmente chamando seu método **IMAPIProp::** GetProps. 
          
      2. Chame o método **IMAPIProp::** SetProps do provedor de host para copiar todas as propriedades recuperadas para o objeto Property do provedor de host. 
      
   2. Se o novo objeto for um destinatário one-off, chame o método **IMAPIProp::** SetProps do provedor de host para definir as seguintes propriedades: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) ao tipo de endereço manipulado pelo provedor.
        
      - **PR\_TemplateID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) para o identificador de modelo dos parâmetros _lpTemplateID_ e _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER ou DT_DISTLIST, conforme apropriado.
    
5. Defina o conteúdo do parâmetro _lppMAPIPropNew_ para apontar para o novo objeto do provedor ou para o objeto Property passado com o parâmetro _lpMAPIPropData_ , dependendo se o provedor determina um objeto wrapped é necessário. 
    
6. Se ocorrer um erro crítico, como uma falha de rede ou uma condição de memória insuficiente, retorne o valor de erro apropriado. Esse valor deve ser propagado para o cliente com a estrutura [MAPIERROR](mapierror.md) apropriada, uma tarefa executada pelo provedor de host. 
    

