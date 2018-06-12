---
title: Definindo as novas propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 68e877568565cfcc30b60e9b21f55b7dc1600b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766394"
---
# <a name="defining-new-mapi-properties"></a>Definindo as novas propriedades MAPI

  
  
**Aplica-se a**: Outlook 
  
Apesar das grande variedade de propriedades fornecido pelo MAPI para uso por clientes e provedores de serviços, MAPI permite novas propriedades a serem criados, se necessário. Alguns dos cenários válidos para definir novas propriedades públicas incluem um cliente de criação de propriedades para oferecer suporte a uma nova classe de mensagem e um provedor de serviços criando novas propriedades expor recursos exclusivos de sistema de mensagens.
  
Geralmente não é válido para um provedor de serviço definir novas propriedades para uma classe de objeto ou mensagem MAPI existente. Um dos principais benefícios do uso de MAPI é que formatos para um grande número de elementos estiver configurados, permitindo que os usuários perfeitamente misturar e combinar de sistema de mensagens e identificadores standard provedores de serviços. Provedores de serviços que usam propriedades fora do padrão não funcionam bem com outros provedores de serviços. 
  
Os clientes podem criar conteúdas propriedades para novas classes de mensagem por:
  
- Usando os identificadores de propriedade em um intervalo designado para propriedades de conteúdo de específicas de classe de mensagem.
    
    - Ou -
    
- Usando propriedades nomeadas. 
    
A primeira opção é preferível porque nem todos os provedores de serviço oferecem suporte a propriedades nomeadas. MAPI define dois intervalos separados para clientes a ser usado para novas propriedades de conteúdo específicos de classe da mensagem:
  
- 0x6800 para 0x7BFF transmittable propriedades
    
- 0x7C00 para 0x7FFF para as propriedades de nontransmittable
    
Identificadores de propriedade devem se enquadram em intervalos predefinidos para ajudar a evitar conflitos entre as propriedades definidas por diferentes fornecedores ou usuários. No entanto, os usuários das propriedades nesses intervalos não podem fazer suposições como para o comportamento das propriedades. Cada cliente que cria uma nova classe de mensagem tem acesso a esses intervalos; uma propriedade com identificador _xxxx_ pode significar um comportamento para uma classe de mensagem e outro comportamento para outra classe de mensagem. 
  
Propriedades nomeadas são usadas para garantir que uma propriedade específica é exclusiva para uma classe de mensagem. Identificadores de propriedade nomeada iniciar no intervalo 0x8000. Clientes definem um ou mais nomes e, em seguida, chame o método de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) do armazenamento de mensagens para associar um identificador de cada nome. Propriedades nomeadas podem ser usadas por clientes ou provedores de serviço para definir novas propriedades para qualquer objeto, somente se o proprietário do objeto oferece suporte a propriedades nomeadas. Os usuários dessas propriedades chamadas **GetIDsFromNames** e um método **IMAPIProp** relacionado, [GetNamesFromIDs](imapiprop-getnamesfromids.md), para mapear entre um nome e seu identificador.
  
Todas as propriedades, novas ou existentes, deverá usar o conjunto de tipos de propriedade predefinida. Não não possível adicionar novos tipos de propriedade e tipos existentes não podem ser modificados ou excluídos. Propriedades de simples, pequenas, como propriedades de caractere único ou 16 bits inteiro, podem ser armazenadas em qualquer tipo apropriado. Por exemplo, inteiros podem ser armazenados como **ULONG** e cadeias de caracteres podem ser armazenadas como **PT_STRING8**. 
  
Use o tipo **PT_BINARY** para indicar uma matriz de bytes contado. Esse tipo de propriedade é útil para estender os tipos de dados que podem ser armazenados em um objeto. Bytes são transmitidas em sequência e não sejam feitas suposições sobre o significado dos dados. Quando um aplicativo cliente lê dados tal propriedade, os dados são inalterados desde como ele foi armazenado. O cliente deve executar qualquer byte necessário permutação ao mover dados entre CPUs. 
  
## <a name="see-also"></a>Confira também



[Vis�o geral da propriedade MAPI](mapi-property-overview.md)

