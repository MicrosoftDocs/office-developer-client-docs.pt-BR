---
title: Bem-vindo à referência auxiliar do Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: A referência auxiliar do Outlook contém conteúdo conceitual e documentação de referência de quatro conjuntos de APIs, amostras de código e uma instalação redistribuível que permite aos desenvolvedores de a extensão e integração com o Outlook. APIs nesta referência são expostas pelo Outlook para extensibilidade, fora do modelo de objeto do Outlook.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384553"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Bem-vindo à referência auxiliar do Outlook

A referência auxiliar do Outlook contém conteúdo conceitual e documentação de referência de quatro conjuntos de APIs, amostras de código e uma instalação redistribuível que permite aos desenvolvedores de a extensão e integração com o Outlook. APIs nesta referência são expostas pelo Outlook para extensibilidade, fora do modelo de objeto do Outlook. 
  
Se você está começando a desenvolver soluções para o Outlook, confira [Selecionando uma API e tecnologia para desenvolver soluções para o Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar as APIs e tecnologias mais adequadas às suas necessidades. 

Para obter informações específicas sobre o modelo de objeto do Outlook, confira a [referência do Outlook VBA](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Para obter informações específicas sobre a API de MAPI (Messaging) com suporte no Outlook, confira a [referência MAPI do Outlook](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Conceitual 

A discussão conceitual inclui os assuntos a seguir:
  
- [Sobre as configurações antispam](about-anti-spam-settings.md)
    
- [Gerenciar o download de mensagens de contas POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Localizar o histórico de download de mensagens de uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Analisar o histórico de download de mensagens de uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Sobre a resolução de conflitos de tipos de itens personalizados](about-conflict-resolution-for-custom-item-types.md)
    
- [Sobre o último tempo de atualização de um catálogo de endereços offline](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Sobre como registrar um novo domínio para configuração automática](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Sobre solicitações de reunião como atualizações informativas e atualizações completas](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [Sobre a alteração da base de calendários programaticamente para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (há também um instalador redistribuível de ferramentas de base de calendários de terceiros, que funciona para as versões anteriores do Outlook, como o Outlook 2010. Para baixar o instalador, confira [Outlook 2010: instalador redistribuível de referência auxiliar e arquivo de cabeçalho de calendários base](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Referências

O conteúdo de referência inclui o seguinte:
  
- As [APIs exportadas pelo Outlook](about-apis-exported-by-outlook.md) incluem funções e estruturas de dados que foram originalmente implementadas para uso interno e agora exibidas para uso público. 
    
- As [API de gerenciamento de conta](about-the-account-management-api.md) fornecem acesso às informações da conta de usuário e as notificações de alterações de conta. 
    
- As [API de camada de degradação de dados](about-the-data-degradation-layer-api.md)dão suporte aos clientes para acessar um item do Outlook em um formato de caractere preferencial em vez do formato de caractere nativo do objeto. 
    
- As [disponibilidade API](about-the-free-busy-api.md) fornece informações de status de disponibilidade sobre contas de usuários específicos em um intervalo de tempo específico. 

## <a name="sample-tasks"></a>Tarefas de exemplo

Tarefas de instruções de exemplo na referência auxiliar do Outlook incluem o seguinte:
    
- [Determinar se um item do Outlook foi modificado mas não salvo (referência do Outlook auxiliar)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Ler propriedades de fuso horário de um compromisso](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Especificar se deseja exibir a imagem de um contato no Outlook (referência auxiliar do Outlook)](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Usar o tempo relativo para acessar dados de disponibilidade](how-to-use-relative-time-to-access-free-busy-data.md)
    
A referência para cada API lista as constantes, definições de tipo e interfaces que o desenvolvedor deve implementar para usar a funcionalidade adicional.
  
> [!NOTE]
> Os desenvolvedores devem implementar essas APIs somente como é documentados nessa referência. Determinados membros de interface e parâmetros de método são designados como espaços reservados porque eles são reservados para uso interno do Outlook e estão sujeitos a alterações sem aviso prévio. 
  

