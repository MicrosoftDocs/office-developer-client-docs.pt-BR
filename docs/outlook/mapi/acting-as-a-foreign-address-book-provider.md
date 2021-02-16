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
  
Um provedor estrangeiro é um provedor de agendas que: 
  
- Atribui identificadores de modelo a seus destinatários.
    
- Dá suporte [ao método IABLogon::OpenTemplateID.](iablogon-opentemplateid.md) 
    
- Fornece código para manter destinatários existentes nos contêineres de outros provedores de agendas de endereços conhecidos como provedores de host. Esse código envolve um objeto de propriedade, normalmente uma implementação de interface **IMAPIProp,** que envolve um objeto de propriedade do provedor de host. 
    
Atuar como um provedor estrangeiro é uma função opcional; nem todos os provedores precisam dar suporte a identificadores de modelo e seu código relacionado. Implemente seu provedor como um provedor estrangeiro se você quiser manter o controle sobre destinatários que os provedores de host criam usando modelos fornecidos por seu provedor. 
  
O formato que seu provedor usa para seus identificadores de entrada também pode ser usado para seus identificadores de modelo. Os identificadores de modelo devem incluir **o MAPIUID** registrado do provedor para habilitar o MAPI para vincular com êxito os destinatários aos provedores apropriados. 
  
O MAPI chama o método **IABLogon::OpenTemplateID** do provedor quando um provedor de host chama [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). O provedor de host passa o identificador de modelo do destinatário no parâmetro  _lpTemplateID_ em sua chamada para **IMAPISupport::OpenTemplateID**. O MAPI determina que o identificador do modelo pertence ao seu provedor, combinando o [MAPIUID](mapiuid.md) no identificador de modelo com o **MAPIUID** que seu provedor registrou no momento do logon. O MAPI encaminha a chamada do provedor de host para seu provedor por meio do **método IABLogon::OpenTemplateID.** 
  
O provedor de host também passa um ponteiro para sua implementação de objeto de propriedade para o destinatário no parâmetro  _lpMAPIPropData,_ um identificador de interface no parâmetro  _lpInterface_ que corresponde ao tipo de implementação de interface passada  _em lpMAPIPropData_ e um sinalizador opcional, FILL_ENTRY. Seu provedor deve retornar no parâmetro  _lppMAPIPropNew_ um ponteiro para uma implementação de objeto de propriedade do tipo especificado em  _lpInterface_. O ponteiro retornado pode ser para o objeto de propriedade de empacotado implementado pelo provedor ou para o objeto fornecido pelo provedor de host em  _lpMAPIPropData_. Seu provedor deve retornar um ponteiro de objeto de propriedade com retorno quando:
  
- A tabela de exibição do destinatário contém controles de caixa de listagem.
    
- O endereço de email do destinatário deve ser montado a partir de dados em vários controles de tabela de exibição.
    
- Seu provedor emite notificações de tabela de exibição.
    
O FILL_ENTRY sinalizador indica ao provedor que o provedor de host exige que todas as propriedades do destinatário sejam atualizadas. Seu provedor é necessário para atender a essa solicitação.
  
Quando um provedor de host chama o método **OpenTemplateID** do provedor, o provedor pode: 
  
- Atualize periodicamente os dados de uma entrada copiada.
    
- Mantenha uma entrada copiada sincronizada com seu original, como quando uma entrada do livro de endereços é copiada para o livro de endereços pessoal.
    
- Implemente a funcionalidade que não pode ser implementada pelo provedor de host, como preencher dinamicamente caixas de listagem na tabela de detalhes da entrada copiada dos dados em um servidor.
    
- Controlar a interação entre as propriedades em uma entrada copiada ou modelo instariado. Por exemplo, calcular **PR_EMAIL_ADDRESS** de outras propriedades exibidas na tabela de detalhes. 
    
Os dois primeiros itens são exemplos de tarefas que não exigem que seu provedor fornecer um objeto de propriedade empacotado — uma implementação de **IMAPIProp** baseada na implementação do provedor de host. Seu provedor pode simplesmente atualizar as propriedades conforme necessário e retornar, definindo o parâmetro _lppMAPIPropNew_ para apontar para o ponteiro passado pelo provedor de host no parâmetro _lpMAPIPropData._ 
  
As duas segundas tarefas exigem que seu provedor retorne ao provedor de host um objeto de propriedade que envolve o objeto do provedor de host com funcionalidade adicional, como a capacidade de exibir uma folha de propriedades para a entrada. Esse objeto de propriedade será um usuário de mensagens ou uma lista de distribuição, dependendo do tipo de objeto passado pelo provedor de host no parâmetro _lpMAPIPropData_ e indicado pelo identificador de interface no parâmetro _lpInterface._ Se o _parâmetro lpMAPIPropData_ aponta para um usuário de mensagens, o objeto de propriedade de empacotamento do provedor deve ser uma implementação **IMailUser.** Se _lpMAPIPropData aponta para_ uma lista de distribuição, ele deve ser uma implementação de **IDistList.** 
  
O objeto de propriedade quebrada de seu provedor intercepta chamadas de método **IMAPIProp** para executar manipulação específica de contexto do destinatário do provedor de host o objeto que ele está envolvendo. MAPI only has one requirement for wrapped property objects: all calls to [IMAPIProp::OpenProperty](imapiprop-openproperty.md) requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property should be passed to the host provider. A implementação do provedor pode usar a tabela retornada para interceptar as notificações da tabela de exibição ou adicionar suas próprias, se necessário. 
  
A lista a seguir inclui tarefas que são normalmente implementadas no objeto de propriedade empacotado implementado por provedores externos:
  
- Valores de propriedade de pré-processamento e pós-processamento para o destinatário do host [em IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Manipular detalhes exibem controles de tabela, como botões e caixas de listagem, **em IMAPIProp::OpenProperty**.
    
- Validando ou manipulando valores de propriedade para o destinatário do host [em IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Calculando as propriedades necessárias, **como PR_EMAIL_ADDRESS** e verificando se todas as propriedades necessárias foram definidas antes de salvar o destinatário do host em [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Para implementar IABLogon::OpenTemplateID
  
1. Verifique se o identificador de modelo passado com o parâmetro  _lpTemplateID_ é válido e está em um formato que seu provedor reconhece. Se não estiver, falhe e retorne MAPI_E_INVALID_ENTRYID. 
    
2. Crie um objeto do tipo indicado pelo identificador do modelo, seja um usuário de mensagens, uma lista de distribuição ou um destinatário único. 
    
3. Chame o **método IUnknown::AddRef** no objeto de propriedade do provedor de host, que é o objeto apontado pelo parâmetro _lpMAPIPropData._ 
    
4. Se o  _parâmetro ulTemplateFlags_ for definido como FILL_ENTRY: 
    
   1. Se o novo objeto for um usuário de mensagens ou uma lista de distribuição:
      
      1. Recupere todas as propriedades do novo objeto, possivelmente chamando seu **método IMAPIProp::GetProps.** 
          
      2. Chame o método **IMAPIProp::SetProps** do provedor de host para copiar todas as propriedades recuperadas para o objeto de propriedade do provedor de host. 
      
   2. Se o novo objeto for um destinatário único, chame o método **IMAPIProp::SetProps** do provedor de host para definir as seguintes propriedades: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço manipulado pelo provedor.
        
      - **PR \_ TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) para o identificador de modelo dos parâmetros _lpTemplateID_ e _cbTemplateID._ 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER ou DT_DISTLIST, conforme apropriado.
    
5. De definir o conteúdo do parâmetro  _lppMAPIPropNew_ para apontar para o novo objeto do provedor ou para o objeto de propriedade passado com o parâmetro  _lpMAPIPropData,_ dependendo se o provedor determinar um objeto de empacotamento é necessário. 
    
6. Se ocorrer um erro crítico, como uma falha de rede ou uma condição de falta de memória, retorne o valor de erro apropriado. Esse valor deve ser propagado para o cliente com a estrutura [MAPIERROR](mapierror.md) apropriada, uma tarefa executada pelo provedor de host. 
    

