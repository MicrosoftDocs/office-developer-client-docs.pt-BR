---
title: Visão geral da referência de MAPI do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: 'Última modificação: 1 de fevereiro de 2013'
localization_priority: Priority
ms.openlocfilehash: dc743824cf96800c32d4b4006ae86fbff0bd48a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348493"
---
# <a name="outlook-mapi-reference-overview"></a>Visão geral da referência de MAPI do Outlook

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico fornece informações gerais sobre a documentação de referência de MAPI do Outlook 2013.
  
## <a name="about-this-documentation"></a>A respeito desta documentação

Esta documentação se aplica à implementação da API de mensagens (MAPI) no Microsoft Outlook 2013. 
  
Antes do Microsoft Office Outlook 2007, a Referência para o programador de MAPI fazia parte da documentação do Microsoft Exchange.
  
> [!NOTE]
> Como o Exchange reduziu a ênfase no uso de MAPI desde o Microsoft Exchange Server 2007, o suporte para a implementação do Exchange ficou limitado. 
  
A implementação de MAPI do Outlook é diferente em relação à do Microsoft Exchange. A implementação do Outlook é otimizada para execução em computadores cliente e enfatiza a baixa latência. A implementação do Exchange se destina aos servidores em que uma alta disponibilidade e vários threads melhores são importantes.
  
Use esta documentação para aplicativos em execução nos sistemas de usuários finais. No caso de aplicativos para servidores, use a implementação de MAPI do Exchange, caso adequado, ou as APIs atuais do Exchange, como os Serviços Web do Exchange. Para saber mais sobre os Serviços Web do Exchange, confira [Referência de Serviços Web do Exchange](https://msdn.microsoft.com/library/bb204119.aspx).
  
Talvez seja possível criar aplicativos que funcionem com as implementações de MAPI do Outlook ou do Exchange. Por exemplo, MFCMAPI funciona adequadamente em qualquer plataforma. As implementações têm muitos recursos comuns, mas há diferenças óbvias e sutis. Teste cuidadosamente nas duas plataformas, caso deseje que o aplicativo funcione em todos os ambientes. Este teste exigirá dois sistemas porque não há suporte para a execução de duas implementações na mesma instalação do sistema operacional.
  
Lembre-se de que a MAPI é apropriada para o acesso de baixo nível aos dados em um armazenamento MAPI ou para a criação de um provedor de catálogo de endereços, de transporte ou de armazenamento de mensagens. Como o MAPI ignora a lógica comercial do Outlook, considere também o uso do modelo de objeto do Outlook, quando avaliar as APIs para a criação da solução. O modelo de objeto do Outlook encapsula a lógica comercial do Outlook, mas não é adequado para o código de vários threads, para provedores de sincronização nem para aplicativos de serviço Windows.
  
Saiba mais sobre as novidades desta edição nos tópicos a seguir:
  
- [Novidades desta edição](what-s-new-in-this-edition.md)
    
- [Elementos de API preteridos nesta edição](api-elements-deprecated-in-this-edition.md)
    
Se você estiver começando a desenvolver aplicativos MAPI para o Outlook, confira os tópicos a seguir:
  
- [Escolher uma API ou tecnologia para o desenvolvimento de soluções para o Outlook 2013](https://msdn.microsoft.com/library/jj900714.aspx)
    
- [Arquivos de cabeçalho usados com frequência](commonly-used-header-files.md)
    
- [Propriedades usadas com frequência](commonly-used-properties.md)
    
- [Objetos usados com frequência](commonly-used-objects.md)
    
O restante dessa referência é categorizado nos três tipos de informações a seguir:
  
- [Exemplos de MAPI](mapi-samples.md): direciona você para muitos exemplos de código que mostram o uso de vários elementos de API, como implementar provedores MAPI básicos e criar itens do Outlook. 
    
- [Conceitos de MAPI](mapi-concepts.md): explica a arquitetura e os conceitos de MAPI. 
    
- [Referência de MAPI](mapi-reference.md): fornece informações detalhadas sobre as funções, interfaces, estruturas e propriedades no MAPI. 
    
## <a name="see-also"></a>Confira também

- [Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)
- [Amostras de MAPI](mapi-samples.md)
- [Conceitos de MAPI](mapi-concepts.md)

