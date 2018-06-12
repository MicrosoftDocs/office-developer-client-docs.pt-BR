---
title: Atuando como um provedor de catálogo de endereço estrangeiro
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 16c3518ab4efddbd68765d9de94db64b4fdc0b64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766113"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Atuando como um provedor de catálogo de endereço estrangeiro

**Aplica-se a**: Outlook 
  
Um provedor externo é um provedor de catálogo de endereços que: 
  
- Atribui os identificadores de modelo para seus destinatários.
    
- Suporta o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) . 
    
- Código de suprimentos para destinatários que existem nos contêineres de outros provedores de catálogo de endereços conhecidos como provedores de host de manutenção. Este código envolve a um objeto property, normalmente uma implementação de interface de **IMAPIProp** , que distribui um objeto property do provedor de host. 
    
Atuar como um provedor de estrangeiro é uma função opcional; nem todos os provedores precisam suportar os identificadores de modelo e seus códigos relacionados. Implemente o seu provedor como um provedor de estrangeiro se você deseja manter o controle sobre destinatários que criam de provedores de host usando modelos fornecidos pelo seu provedor. 
  
O formato que seu provedor usa para seus identificadores de entrada também pode ser usado para seus identificadores de modelo. Identificadores de modelo devem incluir registrados do seu provedor **MAPIUID** para habilitar MAPI vincular com êxito os destinatários para os provedores de apropriado. 
  
MAPI chama o método de **IABLogon:: OpenTemplateID** do seu provedor quando um provedor de host chamadas [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). O provedor de host passa o identificador de modelo do destinatário no parâmetro _lpTemplateID_ na sua chamada **IMAPISupport::OpenTemplateID**. MAPI determina que o identificador de modelo pertence ao seu provedor combinando o [MAPIUID](mapiuid.md) do identificador de modelo com o seu provedor registrado no momento do logon **MAPIUID** . MAPI encaminha a chamada do provedor de host para o seu provedor por meio do método **IABLogon:: OpenTemplateID** . 
  
O provedor de host também passa um ponteiro para sua implementação do objeto de propriedade para o destinatário no parâmetro _lpMAPIPropData_ , um identificador de interface no parâmetro _lpInterface_ que corresponde ao tipo de implementação de interface passados _lpMAPIPropData_e um sinalizador opcional, FILL_ENTRY. Espera-se que o seu provedor retornar no parâmetro _lppMAPIPropNew_ um ponteiro para uma implementação de propriedade de objeto do tipo especificado no _lpInterface_. O ponteiro retornado pode ser ao objeto de propriedade com quebra implementadas pelo seu provedor ou para o objeto fornecido pelo provedor de host em _lpMAPIPropData_. Seu provedor deve retornar um ponteiro de objeto de propriedade com quebra quando:
  
- Tabela de exibição do destinatário contém controles de caixa de lista.
    
- O endereço de email do destinatário deve ser montado a partir de dados em vários controles de exibição de tabela.
    
- Problemas de seu provedor exibem notificações de tabela.
    
O sinalizador FILL_ENTRY indica ao provedor que o provedor de host exige todas as propriedades do destinatário para serem atualizadas. Seu provedor é necessária para preencher essa solicitação.
  
Quando um provedor de host chama o método **OpenTemplateID** do seu provedor de serviço, talvez seu provedor: 
  
- Atualize periodicamente os dados para uma entrada copiada.
    
- Mantenha uma entrada copiada sincronizada com seu original, como quando uma entrada do catálogo de endereços é copiada para o catálogo de endereços pessoal.
    
- Funcionalidade de implementar que não pode ser implementada pelo provedor de host, como dinamicamente Popular lista caixas na tabela de detalhes da entrada copiada de dados em um servidor.
    
- Controle a interação entre propriedades em uma entrada copiada ou modelo instanciado. Por exemplo, computação **PR_EMAIL_ADDRESS** de outras propriedades exibidas na tabela de detalhes. 
    
Os primeiros dois itens são exemplos de tarefas que não exigem o provedor para fornecer um objeto property com quebra — uma implementação do **IMAPIProp** que baseia-se na implementação do provedor de host. Seu provedor pode simplesmente atualizar as propriedades conforme necessário e retorno, definindo o parâmetro _lppMAPIPropNew_ para apontar para o ponteiro transmitido pelo provedor de host no parâmetro _lpMAPIPropData_ . 
  
As segundo duas tarefas exigem que seu provedor retornar ao provedor de host um objeto de propriedade que envolve o objeto do provedor de host com funcionalidades adicionais, como a capacidade de exibir uma folha de propriedades para a entrada. Este objeto de propriedade será uma lista de distribuição ou usuário mensagens, dependendo do tipo de objeto passado pelo provedor de host no parâmetro _lpMAPIPropData_ e indicado pelo identificador de interface no parâmetro _lpInterface_ . Se o parâmetro _lpMAPIPropData_ aponta para um usuário de mensagens, o objeto de propriedade com quebra do seu provedor deve ser uma implementação **IMailUser** . Se _lpMAPIPropData_ aponta para uma lista de distribuição, ela deve ser uma implementação **IDistList** . 
  
Objeto de propriedade com quebra do seu provedor intercepta as chamadas de método **IMAPIProp** para executar a manipulação de contexto específico de destinatário do provedor de host — o objeto, ele é quebrado. MAPI tem somente um requisito para objetos com quebra property: todas as chamadas para [IMAPIProp::OpenProperty](imapiprop-openproperty.md) solicitando a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) devem ser passadas para o provedor de host. Implementação do seu provedor pode usar a tabela retornada para interceptar exibir notificações de tabela ou adicionar o seu próprio, se necessário. 
  
A lista a seguir inclui as tarefas que são geralmente implementadas no objeto de propriedade com quebra implementado pelos provedores externas:
  
- Pré-processamento e o pós-processamento valores de propriedade para o destinatário de host em [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Detalhes de tratamento de controles de tabela, botões e caixas de listagem, são exibidos no **IMAPIProp::OpenProperty**.
    
- Validando ou manipulação de valores de propriedade para o destinatário de host em [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- As propriedades necessárias, como **PR_EMAIL_ADDRESS** de computação e verificando se todas as propriedades necessárias foram definidas antes de salvar o destinatário de host no [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Para implementar IABLogon:: OpenTemplateID
  
1. Verifique se o identificador de modelo passado com o parâmetro _lpTemplateID_ é válido e se está em um formato que o seu provedor reconheça. Se não for, falhar e retornar MAPI_E_INVALID_ENTRYID. 
    
2. Criar um objeto do tipo indicado pelo identificador de modelo, um usuário de mensagens, lista de distribuição ou destinatário único. 
    
3. Chame o método **AddRef** no objeto de propriedade do provedor de host, que é o objeto apontado pelo parâmetro _lpMAPIPropData_ . 
    
4. Se o parâmetro _ulTemplateFlags_ estiver definido como FILL_ENTRY: 
    
   1. Se o novo objeto for uma lista de usuário ou de distribuição de mensagens:
      
      1. Recupere todas as propriedades do novo objeto, possivelmente chamando seu método **IMAPIProp::GetProps** . 
          
      2. Chame o método de **IMAPIProp::SetProps** do provedor de host para copiar todas as propriedades recuperadas para o objeto de propriedade do provedor de host. 
      
   2. Se o novo objeto for um destinatário único, chame o método de **IMAPIProp::SetProps** do provedor de host para definir as seguintes propriedades: 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) para o tipo de endereço manipuladas pelo seu provedor.
        
      - **PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) para o identificador de modelo dos parâmetros _lpTemplateID_ e _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) para DT_MAILUSER ou DT_DISTLIST, conforme apropriado.
    
5. Defina o conteúdo do parâmetro _lppMAPIPropNew_ para apontar para o novo objeto do seu provedor ou o objeto de propriedade passado com o parâmetro _lpMAPIPropData_ , dependendo se o seu provedor determina que um objeto disposto é necessário. 
    
6. Se ocorrer um erro crítico, como uma falha de rede ou um limite de condição de memória, retorne o valor de erro apropriado. Este valor deve obter propagado ao cliente com a estrutura [MAPIERROR](mapierror.md) apropriado, uma tarefa seja executada pelo provedor de host. 
    

