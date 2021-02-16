---
title: Definindo novas propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 666ee413319765e39e25d586208f764afc93ae6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425012"
---
# <a name="defining-new-mapi-properties"></a>Definindo novas propriedades MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em vez da riqueza das propriedades fornecidas pelo MAPI para uso por clientes e provedores de serviços, o MAPI permite que novas propriedades sejam criadas, se necessário. Alguns dos cenários válidos para definir novas propriedades públicas incluem um cliente que cria propriedades para dar suporte a uma nova classe de mensagens e um provedor de serviços que cria novas propriedades para expor recursos exclusivos do sistema de mensagens.
  
Normalmente, não é válido para um provedor de serviços definir novas propriedades para uma classe de mensagem ou objeto MAPI existente. Um dos principais benefícios de usar o MAPI é que identificadores padrão e formatos para um grande número de elementos do sistema de mensagens são definidos, permitindo que os usuários misturem facilmente e corresponderem aos provedores de serviços. Os provedores de serviços que usam propriedades não padrão não funcionam bem com outros provedores de serviços. 
  
Os clientes podem criar propriedades de conteúdo para novas classes de mensagens:
  
- Usar identificadores de propriedade dentro de um intervalo designado para propriedades de conteúdo específicas da classe de mensagens.
    
    - Ou -
    
- Usando propriedades nomeadas. 
    
A primeira opção é preferível porque nem todos os provedores de serviços suportam propriedades nomeadas. O MAPI define dois intervalos separados para que os clientes usem para novas propriedades de conteúdo específicas da classe de mensagens:
  
- 0x6800 para 0x7BFF propriedades transmitíveis
    
- 0x7C00 para 0x7FFF propriedades nãotransmitíveis
    
Os identificadores de propriedade devem se enquadrar em intervalos predefinidos para ajudar a evitar colisões entre propriedades definidas por diferentes fornecedores ou usuários. No entanto, os usuários das propriedades nesses intervalos não podem fazer suposições sobre o comportamento das propriedades. Cada cliente que cria uma nova classe de mensagem tem acesso a esses intervalos; uma propriedade com o identificador  _xxxx_ pode significar um comportamento para uma classe de mensagem e outro comportamento para outra classe de mensagem. 
  
Propriedades nomeadas são usadas para garantir que uma propriedade específica é exclusiva para uma classe de mensagem. Identificadores de propriedade nomeados começam no 0x8000 intervalo. Os clientes definem um ou mais nomes e, em seguida, chamam o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) do armazenamento de mensagens para associar um identificador a cada nome. Propriedades nomeadas podem ser usadas por clientes ou provedores de serviços para definir novas propriedades para qualquer objeto somente se o proprietário do objeto suportar propriedades nomeadas. Os usuários dessas propriedades chamam **GetIDsFromNames** e um método **IMAPIProp** relacionado, [GetNamesFromIDs,](imapiprop-getnamesfromids.md)para mapear entre um nome e seu identificador.
  
Todas as propriedades, novas ou existentes, devem usar o conjunto de tipos de propriedade predefinidos. Novos tipos de propriedade não podem ser adicionados e tipos existentes não podem ser modificados ou excluídos. Propriedades simples e pequenas, como propriedades de um único caractere ou inteiro de 16 bits, podem ser armazenadas em qualquer tipo apropriado. Por exemplo, os inteiros podem ser armazenados como **ULONG** e as cadeias de caracteres podem ser armazenadas **como PT_STRING8**. 
  
Use o **PT_BINARY** para indicar uma matriz de byte contada. Esse tipo de propriedade é útil para estender os tipos de dados que podem ser armazenados em um objeto. Os bytes são transmitidos em sequência e nenhuma suposição é feita sobre o significado dos dados. Quando um aplicativo cliente lê dados dessa propriedade, os dados não são alterados em termos de como eles foram armazenados. O cliente deve executar qualquer troca de byte necessária ao mover dados entre CPUs. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

