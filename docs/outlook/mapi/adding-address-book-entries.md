---
title: Adicionando entradas do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331875"
---
# <a name="adding-address-book-entries"></a>Adicionando entradas do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para adicionar um usuário de mensagens ou uma lista de distribuição a um contêiner, um cliente chama [IAddrBook:: NewEntry](iaddrbook-newentry.md) ou um provedor chama [IMAPISupport:: NewEntry](imapisupport-newentry.md) com o identificador de entrada do contêiner de destino no parâmetro _lpEIDContainer_ . O MAPI, por sua vez, chama o método [IABContainer:: Createentry](iabcontainer-createentry.md) do contêiner para criar a entrada usando um modelo one-off a partir de uma tabela única. Um modelo one-off permite que o cliente crie um novo destinatário de um tipo específico. A maioria dos campos é editável. O modelo apontado pelo parâmetro _lpEntryID_ pode ser um que seu provedor fornece ou pode ser um modelo de um provedor externo, se seu provedor oferecer suporte a modelos estrangeiros. As implementações de **createentry** para provedores que podem criar destinatários a partir de um modelo externo são sempre mais complexas do que as implementações para provedores que não podem. 
  
 **Para implementar o IABContainer:: createEntry**
  
1. Determine o tipo de identificador de entrada especificado pelo parâmetro _lpEntryID_ . 
    
2. Se o identificador de entrada representar um modelo para um usuário de mensagens, lista de distribuição ou contêiner de catálogo de endereços de propriedade de seu provedor:
    
1. Crie e inicialize o objeto apropriado. O provedor pode definir algumas propriedades iniciais, se desejado. Essas propriedades dependem do tipo de destinatário que está sendo criado. 
    
2. ReTorne um ponteiro para a implementação do objeto no conteúdo do parâmetro _lppMAPIPropEntry_ . 
    
3. Se o identificador de entrada representar um modelo para um provedor estrangeiro:
    
1. Chame [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir o objeto externo. 
    
2. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do objeto, passando NULL para a matriz de marca de propriedade, para recuperar suas propriedades. 
    
3. Edite a matriz de valor de **** propriedade retornada de GetProps alterando a marca de propriedade para PR_NULL para todas as propriedades que não se aplicam ao novo objeto e não devem ser transferidas. 
    
4. Crie um identificador de entrada para o novo objeto. 
    
5. Crie um novo objeto do tipo apropriado, o usuário de mensagens ou a lista de distribuição.
    
6. Inicialize o novo objeto definindo propriedades padrão.
    
7. Verifique se o objeto externo oferece suporte à propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Se o objeto externo suportar **PR_TEMPLATEID**, chame [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para recuperar uma interface de objeto de Propriedade do provedor estrangeiro e definir o conteúdo do parâmetro _lppMAPIPropEntry_ para a propriedade estrangeira implementação do objeto. 
    
9. Se o objeto externo não oferecer suporte a **PR_TEMPLATEID**, defina o conteúdo do parâmetro _lppMAPIPropEntry_ para a implementação do novo objeto do provedor. 
    
10. Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps do objeto apontado pelo parâmetro _lppMAPIPropEntry_ para definir as propriedades apropriadas do objeto externo. 
    

