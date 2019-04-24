---
title: Criar um destinatário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332953"
---
# <a name="creating-a-recipient"></a>Criar um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes criam destinatários quando estão endereçando mensagens e quando estão adicionando entradas a contêineres de catálogos de endereços modificáveis. MAPI fornece três métodos para criar destinatários:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Call **IAddrBook:: CreateOneOff** quando você está criando destinatários a serem usados para endereçar mensagens. **CreateOneOff** cria um identificador de entrada one-off formatado especialmente para ser associado a um endereço de um determinado tipo de endereço. Para obter mais informações sobre identificadores de entrada individuais e únicos, confira [endereços únicos](one-off-addresses.md) e [identificadores de entrada one-off](one-off-entry-identifiers.md).
  
Call **IAddrBook:: NewEntry** quando você está criando destinatários a serem usados para endereçar mensagens ou para adicionar a um contêiner. **NewEntry** tem três pares de parâmetros que contêm identificadores de entrada. Esses parâmetros são descritos da seguinte maneira: 
  
|**Par de parâmetros**|**Descrição**|
|:-----|:-----|
| _cbEidContainer_ e _lpEidContainer_ <br/> |Identificador de entrada para o contêiner no qual a nova entrada deve ser colocada.  <br/> |
| _cbEidNewEntryTpl_ e _lpEidNewEntryTpl_ <br/> |Identificador de entrada do modelo a ser usado para criar a nova entrada.  <br/> |
| _lpcbEidNewEntry_ e _lppEidNewEntry_ <br/> |Identificador de entrada para a nova entrada.  <br/> |
   
Para criar um destinatário para uma mensagem de saída, defina _cbEidContainer_ como zero e _lpEidContainer_ como nulo. **NewEntry** cria um destinatário com um identificador de entrada que está de acordo com o formato one-off, o mesmo tipo de destinatário que é produzido por uma chamada para **IAddrBook:: CreateOneOff**. 
  
Para criar um destinatário a ser inserido em um determinado contêiner, defina _lpEidContainer_ como o identificador de entrada do contêiner e _cbEidContainer_ como o número de bytes no identificador de entrada do contêiner. 
  
Para usar um modelo para criar um destinatário, defina _lpEidNewEntryTpl_ para o identificador de entrada do modelo a ser usado e _cbEidNewEntryTpl_ como a contagem de bytes nesse identificador de entrada. A maioria dos contêineres do catálogo de endereços modificável oferece suporte a um ou mais modelos para a criação de entradas de um tipo específico. Modelos únicos são geralmente, mas nem sempre, caixas de diálogo. A inserção de informações no modelo produz um destinatário com um endereço formatado corretamente para o tipo. 
  
Obtenha o identificador de entrada de modelo de:
  
- A coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) na tabela one-off do contêiner, acessada chamando o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner e especificando **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) como a marca de propriedade e IID_IMAPITable como o identificador de interface. 
    
- As propriedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) do provedor de catálogo de endereços que contêm os identificadores de entrada para o objeto de usuário de mensagens do provedor e modelos de lista de distribuição. 
    
> [!NOTE]
> Não confunda um novo identificador de entrada do modelo de entrada com um tipo diferente de identificador de entrada chamado identificador de modelo. Um identificador de modelo é usado apenas por provedores para manter entradas copiadas de outros provedores; Ele nunca é usado por clientes e não é usado para criar novas entradas. 
  
Para permitir que o usuário determine o tipo de entrada a ser criada, passe zero para _cbEidNewEntryTpl_ e nulo para _lpEidNewEntryTpl_. Quando isso ocorre, **NewEntry** exibe uma caixa de diálogo comum criada a partir da tabela única de MAPI — uma lista hierárquica de todos os modelos suportados por cada provedor de catálogo de endereços no perfil. 
  
Quando um tipo de endereço é determinado, seja por meio da configuração do parâmetro _lpEidNewEntryTpl_ ou de uma seleção pelo usuário da exibição da tabela única, **NewEntry** exibe o modelo correspondente usando sua tabela de exibição. Todos os novos modelos de entrada oferecem suporte à propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Para fazer com que o **NewEntry** retorne o identificador de entrada da entrada criada, passe um endereço válido para os parâmetros _lpcbEidNewEntry_ e _lppEidNewEntry_ . O MAPI coloca o novo identificador de entrada no endereço apontado por _lppEidNewEntry_ e a contagem de bytes do novo identificador de entrada no endereço indicado por _lpcbEidNewEntry_.
  
Chame [IABContainer:: createentry](iabcontainer-createentry.md) para criar um destinatário e salvá-lo em um contêiner de catálogo de endereços específico. Você pode usar esse método somente com contêineres modificáveis, que têm o sinalizador AB_MODIFIABLE definido em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Os provedores de catálogo de endereços com contêineres não modificáveis não dão suporte a esse método. Especifique o identificador de entrada do modelo para criar uma entrada do tipo desejado no parâmetro _lpEntryID_ . 
  
No parâmetro _ulCreateFlags_ , especifique o tipo de verificação de entrada duplicada necessária e se as entradas novas devem ou não ser substituídas. Se **createentry** falhar ao criar um novo objeto devido à verificação de entrada duplicada imposta pelo provedor, não espera ver um erro ou aviso retornado. Sob essas condições, os provedores retornam um código de sucesso. 
  
Se você estiver trabalhando diretamente com um contêiner e souber exatamente os tipos de endereços que o contêiner pode criar, pode chamar **IABContainer:: createentry** e passar o identificador de entrada para o modelo apropriado. O provedor do catálogo de endereços define algumas propriedades padrão iniciais; Você pode chamar **** SetProps para definir outras pessoas. O usuário nunca está envolvido. 
  

