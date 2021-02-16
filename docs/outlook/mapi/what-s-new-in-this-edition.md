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
ms.openlocfilehash: 23a8b84af50cc8a046206ab37144d84c4c9b6d56
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329544"
---
# <a name="whats-new-in-this-edition"></a>Novidades desta edição

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A Referência de MAPI do Microsoft Outlook 2013 foi atualizada para incluir a documentação de vários novos recursos. 
  
## <a name="new-content"></a>Novo conteúdo

O conteúdo foi adicionado para os seguintes recursos:
  
- The [topic Getting Started with the Outlook 2013 MAPI Reference](getting-started-with-the-outlook-mapi-reference.md) has been updated to reference comprehensive information about programming models for your Outlook and MAPI functionality to help you identify the APIs and technologies that are most appropriate for your needs. Os links para o artigo técnico referenciado também foram revisados nos seguintes tópicos: 
    
  - [Referência de MAPI do Outlook](outlook-mapi-reference.md)
    
  - [Visão Geral de Referência de MAPI do Outlook](outlook-mapi-reference-overview.md)
    
- **Exemplo de provedor de armazenamento de** mensagens — O código do provedor de armazenamento [PST](message-store-provider-sample.md) com amostra foi revisado para reconhecer e acomodar o Outlook 2013. Para obter mais informações, consulte Conteúdo Revisado Anteriormente neste tópico. 
    
- **Fluxo de preenchimento** automático — o tópico de [cache Nickname,](nickname-cache.md) anteriormente o formato de arquivo **Nk2**, foi atualizado para refletir as alterações no Outlook 2013, bem como no Outlook 2010. Os tópicos a seguir foram revisados para fornecer informações sobre as diretrizes de desenvolvedor de formato de arquivo .nk2 para Microsoft Outlook 2003/Microsoft Office Outlook 2007 e análise de arquivos binários. Para obter mais informações, consulte Conteúdo Revisado Anteriormente neste tópico.
    
  - [Perfis MAPI](mapi-profiles.md)
    
  - [Cache de apelidos](nickname-cache.md)
    
  - [Fluxo de Preenchimento Automático](autocomplete-stream.md)
    
- **Interfaces**-The [IAddrBook::OpenEntry](iaddrbook-openentry.md) topic documents a method of opening an address book entry and returning a pointer to the interface used to access it. Anteriormente, ela continha um sinalizador no parâmetro  *ulFlags,* **MAPI_GAL_ONLY**, que poderia ser usado somente para abrir a Lista de Endereços Global (GAL) e foi revisado para incluir sua definição.
    
- **Propriedades**— o **PR_CONVERSATION_KEY** propriedade nomeada ( propriedade canônica [PidTagConversationKey](pidtagconversationkey-canonical-property.md)) foi adicionado e está relacionado ao **IPM. Mensagens messageManager** somente no MAPI do Outlook. Os tópicos a seguir relacionados a ele e a documentação do fluxo Transport-Neutral TNEF foram revisados: 
    
  - [Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
    
  - [Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)
    
  - [Mapeamento de atributos TNEF para propriedades MAPI](mapping-of-tnef-attributes-to-mapi-properties.md)
    
  - [attConversationID e attParentID](attconversationid-and-attparentid.md)
    
## <a name="previously-revised-content"></a>Conteúdo revisado anteriormente

O conteúdo foi adicionado em versões anteriores da Referência de MAPI do Outlook para os seguintes recursos:
  
- O Microsoft Outlook 2013 permite cenários de implantação não tradicionais, como lado a lado e Clique para Executar. Esses cenários podem complicar a lógica usada para carregar a biblioteca MAPI adequada. Os desenvolvedores de MAPI agora têm a opção de vincular explicitamente a funções MAPI e podem optar por vincular explicitamente ao stub MAPI do cliente MAPI padrão (por exemplo, Msmapi32.dll do Outlook) sem passar pela biblioteca MAPI e o stub mapi do Windows. Para obter mais informações sobre vinculação explícita em comparação com vinculação implícita, consulte [Link para funções MAPI](how-to-link-to-mapi-functions.md). A **Biblioteca stub MAPI**, postada no site [do CodePlex,](https://mapistublibrary.codeplex.com/) fornece um substituto de drop-in para Mapi32.lib que dá suporte à criação de aplicativos MAPI de 32 bits e 64 bits. 
    
- **Suporte para o Microsoft Outlook de 64** bits — Tópicos de referência para elementos de API aplicáveis foram atualizados para corresponder aos novos arquivos de header que suportam o Outlook de 64 bits. Esses arquivos de header estão disponíveis como download no [Outlook 2010: arquivos de header MAPI.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1) Um novo exemplo de código foi fornecido em Verificar a versão do [Outlook](how-to-check-the-version-of-outlook.md) para mostrar como verificar se a versão instalada do Outlook é do Microsoft Outlook 2010 de 64 bits e foi revisada para o Outlook 2013. Se seu aplicativo MAPI de 32 bits existente for executado em um sistema operacional de 64 bits com o Outlook de 64 bits instalado, você precisará recriar seu aplicativo de 32 bits como um aplicativo de 64 bits. Para obter mais informações sobre o suporte a MAPI para o Outlook de 64 bits, consulte Criando aplicativos MAPI em plataformas de 32 bits e [64 bits.](building-mapi-applications-on-32-bit-and-64-bit-platforms.md)
    
- **Exemplo de provedor de armazenamento de** mensagens — O provedor de armazenamento [PST](message-store-provider-sample.md) com conteúdo de exemplo foi atualizado anteriormente para dar suporte à arquitetura de 64 bits. O tópico De inicialização de um provedor de armazenamento [PST](initializing-a-wrapped-pst-store-provider.md) empacotado agora foi expandido para fornecer informações sobre os "Caminhos PST e Unicode empacotados". 
    
- **Fluxo de Preenchimento** Automático — o tópico de [cache Nickname,](nickname-cache.md) anteriormente o formato de arquivo **Nk2**, foi atualizado para refletir as alterações no Outlook 2013, bem como no Outlook 2010. Informações como a lista de preenchimento automático, que é a lista de nomes que é exibida nas caixas de edição **Para** [](autocomplete-stream.md) , **Cc** e **Cc** enquanto um usuário está compondo um email, agora são salvas no Fluxo de Preenchimento Automático de uma mensagem no computador local em vez de salvá-la em um arquivo como no Outlook 2007. 
    
  - Interagindo com o fluxo de preenchimento automático
    
  - Carregando o fluxo de preenchimento automático
    
  - Salvando o fluxo de preenchimento automático
    
- **Suporte de desligamento** rápido para clientes MAPI — os clientes MAPI agora podem iniciar um desligamento rápido e fazer com que o subsistema de MAPI notifique os provedores carregados para minimizar a perda de dados do desligamento rápido. Interfaces adicionais foram adicionadas para o cliente e o provedor suportarem o desligamento rápido. Para obter mais informações sobre o desligamento rápido, consulte [o Desligamento do Cliente em MAPI.](client-shutdown-in-mapi.md)
    
- **Estrutura de fluxo para definições** de campo para um item do Outlook — a documentação de um fluxo binário para a propriedade [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) foi adicionada. Esta propriedade especifica definições de todos os campos personalizados e configurações de vinculação de dados para campos integrados de um item do Outlook. 
    
- **Substituição de** Armazenamento Pessoal — As interfaces a seguir e seus respectivos métodos foram adicionados para dar suporte à substituição da política PSTDisableGrow de provedores de armazenamento **PSTDisableGrow** do arquivo de Pastas Particulares: 
    
    [IPSTOVERRIDEREQ::IUnknown](ipstoverridereqiunknown.md)
    
    [IPSTOVERRIDE1::IUnknown](ipstoverride1iunknown.md)
    
- **Usando várias contas do Exchange —** a documentação da API do Address Book [MAPI](using-multiple-exchange-accounts.md) foi adicionada. Essa API foi aprimorada para dar suporte a várias contas do Exchange no Microsoft Outlook 2010 e agora inclui o Microsoft Outlook 2013. Para resolver os endereços corretamente com várias contas do Exchange, use as novas funções que usam um contexto de conta para que as chamadas para o livro de endereços pesquisem a conta correta do Exchange. 
    
- **Formatos** de arquivo MAPI as informações de configuração MAPI foram expandidas para explicar como você pode usar caminhos em Registrar Serviços e Provedores de Serviços em [MapiSvc.inf](registering-services-and-service-providers-in-mapisvc-inf.md).
    
- **Propriedades**— As seguintes propriedades marcadas foram adicionadas além da documentação de 38 outras propriedades marcadas e propriedades nomeadas que foram adicionadas anteriormente:
    
  - [PidTagAddressBookChooseDirectoryAutomatically](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md)
    
  - [PidTagAssociatedSharingProvider](pidtagassociatedsharingprovider-canonical-property.md)
    
  - [PidTagRoamingBinary](pidtagroamingbinary-canonical-property.md)
    
  - [PidTagSenderSmtpAddress](pidtagsendersmtpaddress-canonical-property.md)
    
  - [PidTagSentRepresentingSmtpAddress](pidtagsentrepresentingsmtpaddress-canonical-property.md)
    
  - [PidTagStoreEntryIdEmsmdbV1](pidtagstoreentryidemsmdbv1-canonical-property.md)
    
- **Constantes MAPI**— As [constantes MAPI](mapi-constants.md) consolidadas foram expandidas. Em versões anteriores, eles eram distribuídos em vários tópicos, mas agora são coletados em um único tópico para facilitar a descoberta e o uso. Eles também foram expandidos para oferecer uma cobertura mais extensa, incluindo as seguintes seções: 
    
  - Definições para o Exchange Address Book e códigos de erro do armazenamento de mensagens
    
  - Definições para Cotas do Modo Cache de Caixa de Correio do Exchange Server
    
## <a name="see-also"></a>Confira também



[Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)
  
[CodePlex](https://mapistublibrary.codeplex.com/)

