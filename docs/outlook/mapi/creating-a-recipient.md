---
title: Criando um destinatário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e14430d1539b90e089a9dabe1315384050f3dd5e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429583"
---
# <a name="creating-a-recipient"></a>Criando um destinatário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes criam destinatários quando estão endereçando mensagens e quando estão adicionando entradas a contêineres de agendas modificáveis. O MAPI fornece três métodos para criar destinatários:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Chame **IAddrBook::CreateOneOff** quando estiver criando destinatários a serem usados para lidar com mensagens. **CreateOneOff** cria um identificador de entrada único especialmente formatado para ser associado a um endereço de um tipo de endereço específico. Para obter mais informações sobre identificadores de entrada one-off e one-off, consulte [Endereços One-Off](one-off-addresses.md) e [Identificadores de Entrada Único.](one-off-entry-identifiers.md)
  
Chame **IAddrBook::NewEntry** quando você estiver criando destinatários a serem usados para lidar com mensagens ou para adicionar a um contêiner. **NewEntry** tem três pares de parâmetros que contêm identificadores de entrada. Esses parâmetros são descritos da seguinte forma: 
  
|**Par de parâmetros**|**Descrição**|
|:-----|:-----|
| _cbEidContainer_ e  _lpEidContainer_ <br/> |Identificador de entrada do contêiner no qual a nova entrada deve ser colocada.  <br/> |
| _cbEidNewEntryTpl_ e  _lpEidNewEntryTpl_ <br/> |Identificador de entrada do modelo a ser usado para criar a nova entrada.  <br/> |
| _lpcbEidNewEntry_ e  _lppEidNewEntry_ <br/> |Identificador de entrada para a nova entrada.  <br/> |
   
Para criar um destinatário para uma mensagem de saída, de definida  _cbEidContainer_ como zero e  _lpEidContainer_ como NULL. **NewEntry** cria um destinatário com um identificador de entrada que está em conformidade com o formato único, o mesmo tipo de destinatário produzido por uma chamada para **IAddrBook::CreateOneOff**. 
  
Para criar um destinatário a ser inserido em um contêiner específico, de definir  _lpEidContainer_ para o identificador de entrada do contêiner e  _cbEidContainer_ para o número de bytes no identificador de entrada do contêiner. 
  
Para usar um modelo para criar um destinatário, de definir  _lpEidNewEntryTpl_ para o identificador de entrada do modelo a ser usado e  _cbEidNewEntryTpl_ para a contagem de bytes neste identificador de entrada. A maioria dos contêineres do livro de endereços modificável suporta um ou mais modelos para a criação de entradas de um tipo específico. Modelos one-off são normalmente, mas nem sempre, caixas de diálogo. Inserir informações no modelo produz um destinatário com um endereço formatado corretamente para o tipo. 
  
Obtenha o identificador de entrada do modelo em:
  
- A **coluna PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) na tabela única do contêiner, acessada chamando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner e especificando **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) como a marca de propriedade e IID_IMAPITable como o identificador da interface. 
    
- As propriedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) do provedor que reter os identificadores de entrada para o objeto de usuário de mensagens do provedor e modelos de lista de distribuição. 
    
> [!NOTE]
> Não confunda o identificador de entrada de um novo modelo de entrada com um tipo diferente de identificador de entrada chamado identificador de modelo. Um identificador de modelo é usado apenas por provedores para manter entradas copiadas de outros provedores; nunca é usado por clientes e não é usado para criar novas entradas. 
  
Para permitir que o usuário determine o tipo de entrada a ser criada, passe zero para  _cbEidNewEntryTpl_ e NULL para  _lpEidNewEntryTpl_. Quando isso ocorre, **NewEntry** exibe uma caixa de diálogo comum criada a partir da tabela única de MAPI — uma lista hierárquica de todos os modelos suportados por cada provedor de agendas no perfil. 
  
Quando um tipo de endereço é determinado, seja por meio da configuração do parâmetro  _lpEidNewEntryTpl_ ou de uma seleção pelo usuário na exibição de tabela única, **NewEntry** exibe o modelo correspondente usando sua tabela de exibição. Todos os novos modelos de entrada suportam **PR_DETAILS_TABLE** propriedade ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Para que **NewEntry** retorne o identificador de entrada da entrada criada, passe um endereço válido para os parâmetros _lpcbEidNewEntry_ e _lppEidNewEntry._ MAPI coloca o novo identificador de entrada no endereço apontado por  _lppEidNewEntry_ e a contagem de byte do novo identificador de entrada no endereço apontado por  _lpcbEidNewEntry_.
  
Chame [IABContainer::CreateEntry](iabcontainer-createentry.md) para criar um destinatário e salvá-lo em um contêiner de agendamento de endereços específico. Você só pode usar esse método com contêineres modificáveis contêineres que tenham o sinalizador AB_MODIFIABLE definido em sua **propriedade PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Os provedores de agendamento de endereços com contêineres nãomodificáveis não suportam esse método. Especifique o identificador de entrada do modelo para criar uma entrada do tipo desejado no _parâmetro lpEntryID._ 
  
No parâmetro  _ulCreateFlags,_ especifique o tipo de verificação de entrada duplicada necessária e se as entradas novas devem ou não substituir as existentes. Se **CreateEntry** falhar ao criar um novo objeto devido à verificação de entrada duplicada imposta pelo provedor, não espere ver um erro ou aviso retornado. Sob essas condições, os provedores retornam um código de sucesso. 
  
Se você estiver trabalhando diretamente com um contêiner e sabe exatamente os tipos de endereços que o contêiner pode criar, chame **IABContainer::CreateEntry** e passe o identificador de entrada para o modelo apropriado. O provedor de agendamento de endereços define algumas propriedades padrão iniciais; você pode chamar **SetProps para** definir outras. O usuário nunca está envolvido. 
  

