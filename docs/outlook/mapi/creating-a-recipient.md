---
title: Criando um destinatário
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 586c901f-d9f9-44f2-a328-051775a81265
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c596cb219cb1096f186e616c05b8372fef3b42a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766362"
---
# <a name="creating-a-recipient"></a>Criando um destinatário

  
  
**Aplica-se a**: Outlook 
  
Clientes criar destinatários quando eles estão lidando com mensagens e quando eles estão adicionando entradas em contêineres de catálogo de endereços modificável. MAPI fornece três métodos para a criação de destinatários:
  
- [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
    
- [IAddrBook::NewEntry](iaddrbook-newentry.md)
    
- [IABContainer::CreateEntry](iabcontainer-createentry.md)
    
Quando você estiver criando destinatários a serem usadas para mensagens de endereço, chame **IAddrBook::CreateOneOff** . **CreateOneOff** cria um identificador de entrada únicos especialmente formatado a ser associado um endereço de um tipo de endereço específica. Para obter mais informações sobre identificadores de entrada únicos e algo isolado, consulte [Endereços únicos](one-off-addresses.md) e [Únicos identificadores de entrada](one-off-entry-identifiers.md).
  
Chamada **IAddrBook::NewEntry** quando você estiver criando destinatários para ser usado tanto para mensagens de endereços ou adicionar um contêiner. **NewEntry** tem três pares de parâmetros que contêm os identificadores de entrada. Esses parâmetros são descritos a seguir: 
  
|**Par de parâmetro**|**Descrição**|
|:-----|:-----|
| _cbEidContainer_ e _lpEidContainer_ <br/> |Identificador de entrada para o contêiner no qual deve ser colocada a nova entrada.  <br/> |
| _cbEidNewEntryTpl_ e _lpEidNewEntryTpl_ <br/> |Identificador de entrada para o modelo a ser usado para criar a nova entrada.  <br/> |
| _lpcbEidNewEntry_ e _lppEidNewEntry_ <br/> |Identificador de entrada para a nova entrada.  <br/> |
   
Para criar um destinatário de uma mensagem de saída, defina _cbEidContainer_ como zero e _lpEidContainer_ como NULL. **NewEntry** cria um destinatário com um identificador de entrada que está em conformidade com o formato único, o mesmo tipo de destinatário que é produzido por uma chamada para **IAddrBook::CreateOneOff**. 
  
Para criar um destinatário a ser inserido em um contêiner específico, defina _lpEidContainer_ como identificador de entrada do contêiner e o _cbEidContainer_ para o número de bytes em um identificador de entrada do contêiner. 
  
Para usar um modelo para criar um destinatário, defina _lpEidNewEntryTpl_ como o identificador de entrada do modelo a ser usado e _cbEidNewEntryTpl_ à contagem de bytes nesse identificador de entrada. Mais modificável contêineres catálogo de endereços oferecem suporte a um ou mais modelos para criação de entradas de um determinado tipo. Modelos de únicos são geralmente, mas nem sempre, caixas de diálogo. Inserindo informações para um modelo produz um destinatário com um endereço que está formatado corretamente para o tipo. 
  
Obter o identificador de entrada do modelo de qualquer um:
  
- A coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) na tabela de únicos do contêiner, acessada chamando o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner e especificando **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) como a marca de propriedade e IID_IMAPITable como o identificador de interface. 
    
- Um endereço livro **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) do provedor e propriedades de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)) que mantenha os identificadores de entrada para o provedor do objeto de usuário de mensagens e modelos de lista de distribuição. 
    
> [!NOTE]
> Não confunda identificador de entrada do modelo uma entrada nova com um tipo diferente de identificador de entrada chamado um identificador de modelo. Um identificador de modelo é usado apenas por provedores para manter entradas copiadas de outros provedores; ele nunca é usado pelos clientes e ele não é usado para criar novas entradas. 
  
Para habilitar o usuário determinar o tipo de entrada a ser criado, passe zero para _cbEidNewEntryTpl_ e NULL para _lpEidNewEntryTpl_. Quando isso ocorre, **NewEntry** exibe uma caixa de diálogo comuns construída a partir da tabela de únicos do MAPI — uma lista hierárquica de todos os modelos compatíveis com cada provedor de catálogo de endereços no perfil. 
  
Quando um tipo de endereço tiver sido determinado, seja por meio da configuração do parâmetro _lpEidNewEntryTpl_ ou uma seleção pelo usuário da exibição da tabela únicos, **NewEntry** exibe o modelo correspondente usando sua tabela de exibição. Todos os novos modelos de entrada suportam à propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). 
  
Para fazer com que **NewEntry** retornar o identificador de entrada da entrada criada, passe um endereço válido para os parâmetros _lpcbEidNewEntry_ e _lppEidNewEntry_ . MAPI coloca o novo identificador de entrada no endereço apontado pela _lppEidNewEntry_ e a contagem de bytes do identificador de entrada de novo no endereço apontado pela _lpcbEidNewEntry_.
  
Chame [IABContainer::CreateEntry](iabcontainer-createentry.md) para criar um destinatário e salvá-lo em um contêiner de catálogo de endereços particular. Você pode usar esse método somente com contêineres modificáveis — contêineres que tenham o AB_MODIFIABLE sinalizador será definido em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)). Provedores de catálogo de endereços com contêineres não modificáveis não suportam este método. Especifique o identificador de entrada do modelo para criar uma entrada do tipo desejado no parâmetro _lpEntryID_ . 
  
No parâmetro _ulCreateFlags_ , especifique o tipo de entrada duplicada verificação necessários e ou não novas entradas devem substituir os existentes. Se **CreateEntry** falhar ao criar um novo objeto devido a verificação de entrada duplicada impostas pelo provedor, não espere ver um erro ou aviso retornado. Sob estas condições, provedores de retornam um código de sucesso. 
  
Se você estiver trabalhando diretamente com um contêiner e você sabe exatamente os tipos de endereços que o contêiner pode criar, você pode chamar **IABContainer::CreateEntry** e passar o identificador de entrada para o modelo apropriado. O provedor de catálogo de endereços define algumas propriedades inicial padrão; é possível chamar **SetProps** para definir a outras pessoas. O usuário está envolvido nunca. 
  

