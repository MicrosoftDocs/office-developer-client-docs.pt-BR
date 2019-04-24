---
title: O que há de novo nesta edição
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329544"
---
# <a name="whats-new-in-this-edition"></a>O que há de novo nesta edição

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A referência de MAPI do Microsoft Outlook 2013 foi atualizada para incluir documentação de vários novos recursos. 
  
## <a name="new-content"></a>Novo conteúdo

O conteúdo foi adicionado para os seguintes recursos:
  
- O tópico de [introdução à referência de MAPI do outlook 2013](getting-started-with-the-outlook-mapi-reference.md) foi atualizado para fazer referência a informações abrangentes sobre modelos de programação para sua funcionalidade do Outlook e MAPI para ajudá-lo a identificar as APIs e tecnologias mais apropriado para suas necessidades. Os links para o artigo técnico referenciado também foram revisados nos seguintes tópicos: 
    
  - [Referência de MAPI do Outlook](outlook-mapi-reference.md)
    
  - [Visão Geral de Referência de MAPI do Outlook](outlook-mapi-reference-overview.md)
    
- **Exemplo de provedor de repositório de mensagens**— o código de [exemplo de provedor de repositório PST encapsulado](message-store-provider-sample.md) foi revisado para reconhecer e acomodar o Outlook 2013. Para obter mais informações, consulte conteúdo reVisado anteriormente neste tópico. 
    
- **Fluxo de preenchimento automático**— o tópico [cache de Alcunha](nickname-cache.md) , anteriormente o **formato de arquivo Nk2**, foi atualizado para refletir as alterações no Outlook 2013, bem como no Outlook 2010. Os tópicos a seguir agora foram revisados para fornecer informações sobre o formato de arquivo. nk2 diretrizes de desenvolvedor para o Microsoft Outlook 2003/Microsoft Office Outlook 2007 e análise de arquivo binário. Para obter mais informações, consulte conteúdo reVisado anteriormente neste tópico.
    
  - [Perfis MAPI](mapi-profiles.md)
    
  - [Cache de apelidos](nickname-cache.md)
    
  - [Fluxo de preenchimento automático](autocomplete-stream.md)
    
- **Interfaces**– o tópico [IAddrBook:: OpenEntry](iaddrbook-openentry.md) documenta um método de abrir uma entrada de catálogo de endereços e retornar um ponteiro para a interface usada para acessá-lo. Anteriormente, ele continha um sinalizador no parâmetro *parâmetroulflags* , **MAPI_GAL_ONLY**, que poderia ser usado para abrir a lista de endereços global (GAL), e foi revisado para incluir sua definição.
    
- **Propriedades**– a propriedade nomeada **PR_CONVERSATION_KEY** ([Propriedade canônica PidTagConversationKey](pidtagconversationkey-canonical-property.md)) foi adicionada e relacionada a **IPM. **Mensagens de MessageManager somente no Outlook MAPI. Os seguintes tópicos relacionados a ele e a documentação do Stream do formato de encapsulamento de transporte neutro (TNEF) foram revisados: 
    
  - [Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Mapeamento de atributos TNEF para propriedades MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID e attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Conteúdo reVisado anteriormente

O conteúdo foi adicionado em versões anteriores da referência MAPI do Outlook para os seguintes recursos:
  
- O Microsoft Outlook 2013 permite cenários de implantação não tradicionais, como lado a lado e clique para executar. Esses cenários podem complicar a lógica usada para carregar a biblioteca MAPI apropriada. Os desenvolvedores MAPI agora têm a opção de vincular explicitamente às funções MAPI e podem optar por vincular explicitamente ao stub MAPI do cliente MAPI padrão (por exemplo, Msmapi32. dll do Outlook) sem passar pela biblioteca MAPI e pelo stub MAPI do Windows. Para obter mais informações sobre vinculação explícita em comparação com o vínculo implícito, consulte [link to MAPI Functions](how-to-link-to-mapi-functions.md). A **biblioteca de stub MAPI**, postada no site [codeplex](https://mapistublibrary.codeplex.com/) , fornece uma substituição de redistribuição para Mapi32. lib que oferece suporte à criação de aplicativos MAPI de 32 bits e 64 bits. 
    
- **Suporte para o Microsoft Outlook de 64 bits**— os tópicos de referência para elementos de API aplicáveis foram atualizados para corresponder aos novos arquivos de cabeçalho que dão suporte ao Outlook de 64 bits. Esses arquivos de cabeçalho estão disponíveis como download no [Outlook 2010: Arquivos de cabeçalho MAPI](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Um novo exemplo de código foi fornecido em [verificar a versão do Outlook](how-to-check-the-version-of-outlook.md) para mostrar como verificar se a versão instalada do Outlook é de 64 bits do Microsoft Outlook e foi revisada para o Outlook 2013. Se o seu aplicativo de MAPI de 32 bits existente estiver sendo executado em um sistema operacional de 64 bits com o Outlook de 64 bits instalado, você precisará reconstruir seu aplicativo de 32 bits como um aplicativo de 64 bits. Para obter mais informações sobre o suporte a MAPI para o Outlook de 64 bits, consulte [Building MAPI Applications in 32-bit and 64-bit Platforms](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Exemplo de provedor de repositório de mensagens**— o [provedor de exemplo de repositório PST encapsulado](message-store-provider-sample.md) anteriormente foi atualizado para suportar a arquitetura de 64 bits. O exemplo de [inicialização de um tópico do provedor de repositório PST encapsulado](initializing-a-wrapped-pst-store-provider.md) foi expandido para fornecer informações sobre os "caminhos PST e Unicode encapsulado". 
    
- **Fluxo de preenchimento automático**— o tópico [cache de Alcunha](nickname-cache.md) , anteriormente, o **formato de arquivo Nk2**, foi atualizado para refletir as alterações no Outlook 2013, bem como no Outlook 2010. Informações como a lista de preenchimento automático, que é a lista de nomes que exibe nas caixas de edição **para**, **CC**e **Cco** enquanto um usuário está redigindo um email, agora é salvo no fluxo de [preenchimento automático](autocomplete-stream.md) de uma mensagem no computador local em vez de salvá-lo em um arquivo como no Outlook 2007. 
    
  - Interagir com o fluxo de preenchimento automático
    
  - Carregar o fluxo de preenchimento automático
    
  - Salvando o fluxo de preenchimento automático
    
- **Suporte de desligaMento rápido para clientes MAPI**— os clientes MAPI agora podem iniciar um desligamento rápido e fazer com que o subsistema MAPI notifique os provedores carregados para minimizar a perda de dados do desligamento rápido. Foram adicionadas interfaces adicionais para o cliente e o provedor suportar o desligamento rápido. Para obter mais informações sobre o desligamento rápido, consulte [Client Shutdown in MAPI](client-shutdown-in-mapi.md).
    
- **Estrutura de fluxo para definições de campo para um item do Outlook**— a documentação de um fluxo binário para a propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) foi adicionada. Esta propriedade especifica as definições de todos os campos personalizados e configurações de associação de dados para campos internos de um item do Outlook. 
    
- **Substituição de repositório pessoal**— as seguintes interfaces e seus respectivos métodos foram adicionados para suportar a substituição do arquivo de pastas particulares (PST) provedores de repositórios **PSTDisableGrow** : 
    
    [IPSTOVERRIDEREQ:: IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1:: IUnknown](ipstoverride1iunknown.md)
    
- **Usando várias contas do Exchange**— a documentação da [API do catálogo de endereços MAPI](using-multiple-exchange-accounts.md) foi adicionada. Esta API foi aprimorada para dar suporte a várias contas do Exchange no Microsoft Outlook 2010 e agora inclui o Microsoft Outlook 2013. Para resolver endereços corretamente com várias contas do Exchange, use as novas funções que usam um contexto de conta para que as chamadas ao catálogo de endereços pesquisem a conta correta do Exchange. 
    
- **Formatos de arquivo MAPI**— as informações de configuração MAPI foram expandidas para explicar como você pode usar caminhos no [registro de serviços e provedores de serviços no MapiSvc. inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propriedades**— as seguintes propriedades marcadas foram adicionadas além da documentação para 38 outras propriedades marcadas e propriedades nomeadas que foram adicionadas anteriormente:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**— as [constantes MAPI](mapi-constants.md) consolidadas foram expandidas. Em versões anteriores, elas foram distribuídas em vários tópicos, mas agora são coletadas em um único tópico para facilitar a descoberta e o uso. Eles também foram expandidos para fornecer uma cobertura mais abrangente, incluindo as seguintes seções: 
    
  - Definições de códigos de erro do catálogo de endereços do Exchange e do repositório de mensagens
    
  - Definições para cotas do modo cache de caixa de correio do Exchange Server
    
## <a name="see-also"></a>Confira também



[Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

