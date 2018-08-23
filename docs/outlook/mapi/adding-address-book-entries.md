---
title: Adicionar entradas ao catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590131"
---
# <a name="adding-address-book-entries"></a>Adicionar entradas ao catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para adicionar um usuário de mensagens ou a lista de distribuição para um contêiner, a chamadas de cliente [IAddrBook::NewEntry](iaddrbook-newentry.md) ou um provedor chama [IMAPISupport::NewEntry](imapisupport-newentry.md) com o identificador de entrada do contêiner de destino no parâmetro _lpEIDContainer_ . MAPI por sua vez chama o método de [IABContainer::CreateEntry](iabcontainer-createentry.md) do contêiner para criar a entrada usando um modelo único de uma tabela único. Um modelo único permite que o cliente criar um novo destinatário de um determinado tipo. A maioria dos campos podem ser editada. O modelo apontado pelo parâmetro _lpEntryID_ pode ser uma que seu provedor fornece ou talvez seja um modelo de um provedor estrangeiro, se o provedor oferece suporte a modelos estrangeiro. Implementações de **CreateEntry** para provedores que podem criar destinatários a partir de um modelo estrangeiro sempre são mais complexos que implementações para provedores que não é possível. 
  
 **Para implementar IABContainer::CreateEntry**
  
1. Determine o tipo de identificador de entrada especificada pelo parâmetro _lpEntryID_ . 
    
2. Se o identificador de entrada representa um modelo para um usuário de mensagens, lista de distribuição ou pertencentes ao seu provedor de contêiner de catálogo de endereços:
    
1. Criar e inicializar o objeto apropriado. Seu provedor pode definir algumas propriedades iniciais, se desejado. Essas propriedades dependem do tipo de destinatário que está sendo criado. 
    
2. Retorne um ponteiro para a implementação do objeto, no conteúdo do parâmetro _lppMAPIPropEntry_ . 
    
3. Se o identificador de entrada representa um modelo para um provedor de externo:
    
1. Chame [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o objeto estranho. 
    
2. Chame o método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) , passando NULL para a matriz de marca de propriedade, para recuperar as suas propriedades. 
    
3. Edite a matriz de valores de propriedade retornado de **GetProps** , alterando a marca de propriedade para PR_NULL para todas as propriedades que não serão aplicadas ao novo objeto e não devem ser transferidas. 
    
4. Crie um identificador de entrada para o novo objeto. 
    
5. Criar um novo objeto de apropriada, digite qualquer lista de usuário ou de distribuição de mensagens.
    
6. Inicialize o novo objeto, definindo as propriedades padrão.
    
7. Verifique se ou não um objeto estranho suporta a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Se o objeto estranho suporta **PR_TEMPLATEID**, chame [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar uma interface de objeto de propriedade do provedor de estrangeira e definir o conteúdo do parâmetro _lppMAPIPropEntry_ para a propriedade foreign implementação de objeto. 
    
9. Se o objeto estranho não oferece suporte a **PR_TEMPLATEID**, defina o conteúdo do parâmetro _lppMAPIPropEntry_ a implementação do seu provedor do novo objeto. 
    
10. Chame o método [IMAPIProp::SetProps](imapiprop-setprops.md) do objeto apontado pelo parâmetro _lppMAPIPropEntry_ para definir as propriedades adequadas de um objeto estranho. 
    

