---
title: Adicionando entradas do Livro de Endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421337"
---
# <a name="adding-address-book-entries"></a>Adicionando entradas do Livro de Endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para adicionar um usuário de mensagens ou uma lista de distribuição a um contêiner, um cliente chama [IAddrBook::NewEntry](iaddrbook-newentry.md) ou um provedor chama [IMAPISupport::NewEntry](imapisupport-newentry.md) com o identificador de entrada do contêiner de destino no parâmetro _lpEIDContainer._ O MAPI, por sua vez, chama o método [IABContainer::CreateEntry](iabcontainer-createentry.md) do contêiner para criar a entrada usando um modelo único de uma tabela única. Um modelo único permite que o cliente crie um novo destinatário de um tipo específico. A maioria dos campos é editável. O modelo apontado pelo parâmetro  _lpEntryID_ pode ser aquele que seu provedor fornece ou pode ser um modelo de um provedor estrangeiro, se seu provedor oferece suporte a modelos externos. Implementações de **CreateEntry** para provedores que podem criar destinatários a partir de um modelo externo são sempre mais complexas do que implementações para provedores que não podem. 
  
 **Para implementar IABContainer::CreateEntry**
  
1. Determine o tipo de identificador de entrada especificado pelo parâmetro _lpEntryID._ 
    
2. Se o identificador de entrada representar um modelo para um usuário de mensagens, lista de distribuição ou contêiner de agendamento de endereço pertencente ao seu provedor:
    
1. Crie e inicialize o objeto apropriado. Seu provedor pode definir algumas propriedades iniciais, se desejado. Essas propriedades dependem do tipo de destinatário que está sendo criado. 
    
2. Retorne um ponteiro para a implementação do objeto no conteúdo do parâmetro _lppMAPIPropEntry._ 
    
3. Se o identificador de entrada representar um modelo para um provedor estrangeiro:
    
1. Chame [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o objeto externo. 
    
2. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do objeto, passando NULL para a matriz de marca de propriedade, para recuperar suas propriedades. 
    
3. Edite a matriz de valores de propriedade retornada de **GetProps** alterando a marca de propriedade para PR_NULL para todas as propriedades que não se aplicarão ao novo objeto e não devem ser transferidas. 
    
4. Crie um identificador de entrada para o novo objeto. 
    
5. Crie um novo objeto do tipo apropriado, seja usuário de mensagens ou lista de distribuição.
    
6. Inicialize o novo objeto definindo as propriedades padrão.
    
7. Verifique se o objeto externo dá suporte ou não **à PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) . 
    
8. Se o objeto externo suportar **PR_TEMPLATEID**, chame [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para recuperar uma interface de objeto de propriedade do provedor estrangeiro e definir o conteúdo do parâmetro  _lppMAPIPropEntry_ para a implementação de objeto de propriedade estrangeira. 
    
9. Se o objeto externo não suportar **PR_TEMPLATEID**, de definir o conteúdo do parâmetro  _lppMAPIPropEntry_ para a implementação do novo objeto pelo provedor. 
    
10. Chame o [método IMAPIProp::SetProps](imapiprop-setprops.md) do objeto apontado pelo parâmetro  _lppMAPIPropEntry_ para definir as propriedades apropriadas do objeto externo. 
    

