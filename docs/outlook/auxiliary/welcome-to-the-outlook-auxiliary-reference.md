---
title: Bem-vindo à referência auxiliar do Outlook
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Referência auxiliar do Outlook contém conteúdo conceitual e documentação de referência para quatro conjuntos de APIs, exemplos de códigos e um instalador redistribuível que permitem aos desenvolvedores estender e integração com o Outlook. APIs nesta referência são expostos pelo Outlook para extensibilidade, fora do modelo de objeto do Outlook.
ms.openlocfilehash: 5f289a1be8fe5d10ddac37394c940f2627415136
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766083"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Bem-vindo à referência auxiliar do Outlook

Referência auxiliar do Outlook contém conteúdo conceitual e documentação de referência para quatro conjuntos de APIs, exemplos de códigos e um instalador redistribuível que permitem aos desenvolvedores estender e integração com o Outlook. APIs nesta referência são expostos pelo Outlook para extensibilidade, fora do modelo de objeto do Outlook. 
  
Se você é novo no desenvolvimento de soluções para o Outlook, consulte [selecionando um API ou tecnologia para desenvolver soluções do Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) para identificar as APIs e tecnologias que são mais apropriadas para suas necessidades. 

Para obter informações específicas sobre o modelo de objeto do Outlook, consulte a [referência VBA do Outlook](http://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Para obter informações específicas sobre Messaging API (MAPI) suportados pelo Outlook, consulte a [Referência MAPI do Outlook](http://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Conceituais 

A abordagem conceitual inclui os seguintes assuntos:
  
- [Sobre as configurações do anti-spams](about-anti-spam-settings.md)
    
- [Gerenciando mensagem downloads para contas POP3](managing-message-downloads-for-pop3-accounts.md)
    
- [Localizando o histórico de download de mensagens para uma conta POP3](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Analisar o histórico de download de mensagens para uma conta POP3](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Sobre a resolução de conflito para tipos de item personalizada](about-conflict-resolution-for-custom-item-types.md)
    
- [Sobre a hora da última atualização de um catálogo de Endereços Offline](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Sobre como registrar um novo domínio para configuração automática](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Sobre as solicitações de reunião como atualizações informativas e completo](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [Sobre REBASE de calendários programaticamente para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (Também há um instalador redistribuível para ferramentas de REBASE de calendário de terceiros, que funciona para versões anteriores do Outlook também desde o Outlook 2010. Para baixar o instalador, consulte [Outlook 2010: instalador redistribuível de referência auxiliar e o arquivo de cabeçalho para a alteração da Base de calendários](http://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [Sobre TZDEFINITION persistente em um fluxo para confirmar uma propriedade binária](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Refer�ncia

O conteúdo de referência inclui o seguinte:
  
- As [APIs exportada pelo Outlook](about-apis-exported-by-outlook.md) incluem funções e estruturas de dados que foram implementadas originalmente para uso interno e agora são expostas para uso público. 
    
- A [API de gerenciamento de conta](about-the-account-management-api.md) fornece acesso a informações de conta de usuário e notificações de alterações de conta. 
    
- A [API de camada de degradação dados](about-the-data-degradation-layer-api.md) oferece suporte a clientes que acessam um item do Outlook em um formato de caracteres preferencial em vez de formato de caractere nativo do objeto. 
    
- A [API de Free/Busy](about-the-free-busy-api.md) fornece informações de status livre/ocupado sobre contas de usuários específicos dentro de um intervalo de tempo específico. 

## <a name="sample-tasks"></a>Tarefas de amostra

Tarefas de amostra instruções na referência auxiliar do Outlook incluem o seguinte:
    
- [Determinar se um item do Outlook foi modificado, mas não salvo (referência auxiliar do Outlook)](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analisar um fluxo de uma propriedade binária para ler a estrutura TZREG](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Ler as propriedades de fuso horário de um compromisso](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Especifique se deseja exibir a imagem de um contato no Outlook (referência auxiliar do Outlook)](https://msdn.microsoft.com/en-us/library/office/gg262879.aspx)
    
- [Use o tempo relativo para acessar dados do tipo disponível/ocupado](how-to-use-relative-time-to-access-free-busy-data.md)
    
A referência para a API de cada lista de constantes, definições de tipo e interfaces que um desenvolvedor deve implementar para usar a funcionalidade adicional.
  
> [!NOTE]
> Os desenvolvedores devem implementar essas APIs apenas conforme documentado nesta referência. Determinados membros de interface e os parâmetros de método são nomeados como marcadores porque eles são reservados para uso interno do Outlook e estão sujeitos a alteração sem aviso prévio. 
  

