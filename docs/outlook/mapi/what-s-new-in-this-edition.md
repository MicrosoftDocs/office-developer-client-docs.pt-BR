---
title: Novidades desta edição
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a24cad75-1237-469f-b7f3-cbbb88f80d44
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 7325c42fe7e9c1e043609d5503a3782522f76188
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590054"
---
# <a name="whats-new-in-this-edition"></a>Novidades desta edição

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Referência do MAPI do Microsoft Outlook 2013 foi atualizada para incluir a documentação para vários novos recursos. 
  
## <a name="new-content"></a>Novo conteúdo

Conteúdo foi adicionado para os seguintes recursos:
  
- O tópico [Getting Started with a referência do MAPI do Outlook 2013](getting-started-with-the-outlook-mapi-reference.md) foi atualizado para fazer referência a informações abrangentes sobre modelos para a sua funcionalidade do Outlook e MAPI para ajudá-lo a identificar as APIs e tecnologias que são mais de programação apropriado para suas necessidades. Links para o artigo técnico referenciado também foram revisadas nos seguintes tópicos: 
    
  - [Referência de MAPI do Outlook](outlook-mapi-reference.md)
    
  - [Visão Geral de Referência de MAPI do Outlook](outlook-mapi-reference-overview.md)
    
- **Exemplo de mensagem do provedor de repositório**— agora foi revisado o código de [Amostra provedor de repositórios de PST quebrado automaticamente](message-store-provider-sample.md) para reconhecer e para acomodar o Outlook 2013. Para obter mais informações, consulte o conteúdo revisado anteriormente neste tópico. 
    
- **Fluxo de AutoCompletar**— o tópico de [cache de apelidos](nickname-cache.md) , anteriormente o **Formato de arquivo Nk2**, tinha foi atualizado para refletir as alterações no Outlook 2013, bem como o Outlook 2010. Os tópicos a seguir agora foram revisados para fornecer informações sobre as diretrizes de desenvolvedor do formato de arquivo. nk2 para Microsoft Outlook 2003/Microsoft Office Outlook 2007 e análise de arquivos binários. Para obter mais informações, consulte o conteúdo revisado anteriormente neste tópico.
    
  - [Perfis MAPI](mapi-profiles.md)
    
  - [Cache de apelidos](nickname-cache.md)
    
  - [Fluxo de preenchimento automático](autocomplete-stream.md)
    
- **Interfaces**-tópico [IAddrBook::OpenEntry](iaddrbook-openentry.md) documenta um método de abertura de uma entrada do catálogo de endereços e retornando um ponteiro para a interface usada para acessá-lo. Conter um sinalizador no parâmetro *ulFlags* , **MAPI_GAL_ONLY**, que pode ser usado para abrir a lista (endereços Global), apenas e foi revisado para incluir sua definição anteriormente.
    
- **Propriedades**— **PR_CONVERSATION_KEY** denominado tópico property ([Propriedade de PidTagConversationKey canônico](pidtagconversationkey-canonical-property.md)) foi adicionado e se relaciona com **IPM. MessageManager** mensagens no Outlook MAPI. Os seguintes tópicos relativos a ela e a documentação do stream Transport-Neutral Encapsulation Format (TNEF) foram revisados: 
    
  - [Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Mapeamento dos atributos de TNEF para propriedades MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID e attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Anteriormente conteúdo revisado

Conteúdo foi adicionado nas versões anteriores da referência do MAPI do Outlook para os seguintes recursos:
  
- Microsoft Outlook 2013 permite cenários de implantação não tradicionais como lado a lado e Click-to-Run. Esses cenários podem complicar a lógica usada para carregar a biblioteca apropriada de MAPI. Desenvolvedores MAPI agora têm a opção de vinculação explicitamente às funções MAPI e podem escolher deseja estabelecer um vínculo explicitamente o fragmento de código MAPI do cliente MAPI padrão (por exemplo, Msmapi32 do Outlook) sem precisar passar pela biblioteca MAPI e o fragmento de código do Windows MAPI. Para obter mais informações sobre a vinculação explícitas em comparação com a vinculação implícita, consulte o [Link para funções de MAPI](how-to-link-to-mapi-functions.md). A **Biblioteca de Stub MAPI**, postado no site do [CodePlex](http://mapistublibrary.codeplex.com/) , fornece uma substituição para soltar para Mapi32.lib que ofereça suporte a criação de aplicativos de MAPI de 32 bits e 64 bits. 
    
- **Suporte para 64 bits Microsoft Outlook**— tópicos de referência para elementos de API aplicáveis foram atualizados para corresponderem aos novos arquivos de cabeçalho que dão suporte ao Outlook de 64 bits. Esses arquivos de cabeçalho estão disponíveis para download em [Outlook 2010: arquivos de cabeçalho de MAPI](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1). Um exemplo de código novo fornecido no [Verificar a versão do Outlook](how-to-check-the-version-of-outlook.md) para mostrar como verificar se a versão instalada do Outlook é o Microsoft Outlook 2010 de 64 bits e foi revisada para o Outlook 2013. Se seu aplicativo existente de MAPI de 32 bits vai estar em execução em um sistema operacional de 64 bits com o Outlook de 64 bits instalado, você precisará recriar seu aplicativo de 32 bits como um aplicativo de 64 bits. Para obter mais informações sobre o suporte MAPI para Outlook de 64 bits, consulte [Compilando aplicativos MAPI em plataformas de 32 bits e 64 bits](building-mapi-applications-on-32-bit-and-64-bit-platforms.md).
    
- **Exemplo de mensagem do provedor de repositório**— o [Provedor de armazenamento de PST quebrado automaticamente exemplo](message-store-provider-sample.md) foi atualizado anteriormente para oferecer suporte a arquitetura de 64 bits. Tópico de [inicializar um provedor de armazenamento de PST quebrado automaticamente](initializing-a-wrapped-pst-store-provider.md) de exemplo agora foi expandido para fornecer informações sobre o "Wrapped PST e caminhos Unicode." 
    
- **Fluxo de AutoCompletar**— o tópico de [cache de apelidos](nickname-cache.md) , anteriormente o **Formato de arquivo Nk2**, foi atualizado para refletir as alterações no Outlook 2013, bem como o Outlook 2010. Informações sobre como a lista de preenchimento automático, que é a lista de nomes que exibe o **para**, **Cc**e **Cco** caixas de edição enquanto um usuário está redigindo um email, agora está salva no [fluxo de preenchimento automático](autocomplete-stream.md) de uma mensagem no computador local em vez de salvá-lo em um arquivo como no Outlook 2007. 
    
  - Interação com o fluxo de preenchimento automático
    
  - Carregando o fluxo de preenchimento automático
    
  - Salvando o fluxo de preenchimento automático
    
- **Suporte de desligamento rápido para clientes MAPI**— clientes MAPI agora podem iniciar um desligamento rápido e fazer com que o subsistema de MAPI notifique provedores carregados para minimizar a perda de dados do fast desligamento. Interfaces adicionais foram adicionados para o cliente e o provedor suportar o desligamento rápido. Para obter mais informações sobre o desligamento rápido, consulte [Desligamento do cliente em MAPI](client-shutdown-in-mapi.md).
    
- **Estrutura de fluxo de definições de campo para um item do Outlook**— documentação para um fluxo binário para a propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) foi adicionada. Esta propriedade especifica as definições de todos os campos personalizados e configurações de associação de dados para campos internos de um item do Outlook. 
    
- **Armazenar pessoais substituir**— as seguintes interfaces e seus respectivos métodos foram adicionados para suportar a substituir a política de **PSTDisableGrow** pastas particulares (. PST) do arquivo repositório provedores: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Usando várias contas do Exchange**— documentação da [API de catálogo de endereços MAPI](using-multiple-exchange-accounts.md) foi adicionada. Essa API foi aprimorado para oferecer suporte a várias contas do Exchange no Microsoft Outlook 2010 e agora inclui o Microsoft Outlook 2013. Para resolver endereços corretamente com várias contas do Exchange, use as novas funções que obtenha um contexto de conta, para que a conta do Exchange correta de pesquisa de chamadas para o catálogo de endereços. 
    
- **Formatos de arquivo de MAPI**— informações de configuração de MAPI foi expandidas para explicar como você pode usar caminhos em [Registrando serviços e provedores de serviços em MAPISVC](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propriedades**— as seguintes propriedades marcadas foram adicionadas além da documentação para outros 38 marcados propriedades e propriedades que anteriormente tinham sido adicionadas nomeadas:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes de MAPI**— foram expandidos consolidada [Constantes de MAPI](mapi-constants.md) . Nas versões anteriores, eles foram distribuídos em um número de tópicos, mas agora são coletados em um único tópico para facilitar descobrir e usar. Eles também foram expandidos para fornecer cobertura mais abrangente, incluindo as seguintes seções: 
    
  - Definições de catálogo de endereços do Exchange e códigos de erro de armazenamento de mensagens
    
  - Cotas do modo de cache de definições de caixa de correio do Exchange Server
    
## <a name="see-also"></a>Confira também



[Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](http://mapistublibrary.codeplex.com/)

