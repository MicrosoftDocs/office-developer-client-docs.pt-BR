---
title: Visão geral da referência de MAPI do Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c126d0c-d7c0-45c0-801c-c9f1e44c9db6
description: '�ltima altera��o: sexta-feira, 1 de fevereiro de 2013'
ms.openlocfilehash: c0d7faaa957167977606cd93800a085d62b214f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768192"
---
# <a name="outlook-mapi-reference-overview"></a>Visão geral da referência de MAPI do Outlook

**Aplica-se a**: Outlook 
  
Este tópico fornece informações gerais sobre a documentação de referência do MAPI do Outlook 2013.
  
## <a name="about-this-documentation"></a>Sobre esta documentação

Esta documentação se aplica à implementação da API do MAPI (Messaging) no Microsoft Outlook 2013. 
  
Anterior para o Microsoft Office Outlook 2007, a referência do programador de MAPI fazia parte da documentação do Microsoft Exchange.
  
> [!NOTE]
> Porque o Exchange tem deemphasized o uso de MAPI desde o Microsoft Exchange Server 2007, o suporte para a implementação do Exchange é limitada. 
  
A implementação do MAPI do Outlook difere de implementação do Microsoft Exchange. A implementação do Outlook é otimizada para execução nos computadores cliente e enfatiza baixa latência. A implementação do Exchange é direcionada para servidores que exigem alta disponibilidade e melhor multithreading são importantes.
  
Use essa documentação para aplicativos executados em sistemas de usuário final. Para aplicativos de servidor, use a implementação do Exchange do MAPI se apropriado ou use APIs atual do Exchange, como serviços Web do Exchange. Para obter mais informações sobre serviços Web do Exchange, consulte a [Referência do Exchange Web Services](http://msdn.microsoft.com/en-us/library/bb204119.aspx).
  
Talvez seja possível escrever aplicativos que funcionam com o Outlook ou o Exchange implementações de MAPI. Por exemplo, o MFCMAPI funciona bem em qualquer uma das plataformas. As implementações tem muitos recursos comuns, mas há diferenças óbvias e sutil. Você precisará testar cuidadosamente em ambas as plataformas, caso você pretenda para seu aplicativo funcionar em todos os ambientes. Esse teste exigirá dois sistemas porque não há suporte para a execução as duas implementações na mesma instalação do sistema operacional.
  
Lembre-se de que o MAPI é apropriado para baixo nível acesso aos dados em um repositório MAPI ou para a criação de um transporte, o armazenamento de mensagens ou o provedor de catálogo de endereços. Como o MAPI ignora a lógica de negócios do Outlook, você também deve considerar o uso do modelo de objeto do Outlook ao avaliar APIs para a criação de sua solução. O modelo de objeto do Outlook encapsulam a lógica de negócios do Outlook, mas não é adequado para código multithread, provedores de sincronização ou aplicativos de serviço do Windows.
  
Para obter informações sobre quais são as novidades nesta edição, consulte os tópicos a seguir:
  
- [Novidades nesta edi��o (em ingl�s)](what-s-new-in-this-edition.md)
    
- [Elementos de API preteridos nesta edi��o](api-elements-deprecated-in-this-edition.md)
    
Se você ainda não conhece para desenvolver aplicativos MAPI para Outlook, consulte os seguintes tópicos:
  
- [Selecionando uma API ou tecnologia para desenvolver soluções do Outlook 2013](http://msdn.microsoft.com/en-us/library/jj900714.aspx)
    
- [Arquivos de cabe�alho usados com freq��ncia](commonly-used-header-files.md)
    
- [Propriedades comumente usadas](commonly-used-properties.md)
    
- [Os objetos mais usados](commonly-used-objects.md)
    
O restante desta referência é categorizado os três tipos de informações a seguintes:
  
- [Amostras de MAPI](mapi-samples.md) - direciona você para muitos exemplos de código que mostram o uso de vários elementos de API e como implementar provedores MAPI básicas e criar itens do Outlook. 
    
- [Conceitos MAPI](mapi-concepts.md) - explica os conceitos e a arquitetura do MAPI. 
    
- [Referência MAPI](mapi-reference.md) - fornece informações detalhadas sobre as funções, interfaces, estruturas e propriedades na MAPI. 
    
## <a name="see-also"></a>Confira também

- [Introdução à Referência de MAPI do Outlook](getting-started-with-the-outlook-mapi-reference.md)
- [Amostras MAPI (em ingl�s)](mapi-samples.md)
- [Conceitos MAPI (em ingl�s)](mapi-concepts.md)

