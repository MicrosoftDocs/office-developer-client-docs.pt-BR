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
  
Apesar da infinidade de propriedades fornecidas pelo MAPI para uso por clientes e provedores de serviço, o MAPI permite que novas propriedades sejam criadas, se necessário. Alguns dos cenários válidos para definir novas propriedades públicas incluem um cliente que cria propriedades para dar suporte a uma nova classe de mensagens e um provedor de serviços criando novas propriedades para expor recursos exclusivos do sistema de mensagens.
  
Normalmente, não é válido para um provedor de serviços definir novas propriedades para um objeto MAPI ou uma classe de mensagem existente. Um dos principais benefícios do uso de MAPI é que os identificadores e formatos padrão de um grande número de elementos do sistema de mensagens estão configurados, permitindo que os usuários misturem e correspondam diretamente aos provedores de serviços. Os provedores de serviços que usam Propriedades fora do padrão não funcionam bem com outros provedores de serviços. 
  
Os clientes podem criar propriedades de conteúdo para novas classes de mensagens:
  
- Usando identificadores de propriedade dentro de um intervalo designado para propriedades de conteúdo específicas de classe de mensagem.
    
    - Ou
    
- Usando propriedades nomeadas. 
    
A primeira opção é preferível porque nem todos os provedores de serviços dão suporte a propriedades nomeadas. MAPI define dois intervalos separados para os clientes usarem para novas propriedades de conteúdo específicas da classe de mensagens:
  
- 0x6800 para 0x7BFF para propriedades de transmittable
    
- 0x7C00 para 0x7FFF para propriedades não transmittable
    
Os identificadores de propriedade devem estar em intervalos predefinidos para ajudar a evitar colisões entre as propriedades definidas por diferentes fornecedores ou usuários. No enTanto, os usuários das propriedades nesses intervalos não podem fazer suposições como o comportamento das propriedades. Todos os clientes que criam uma nova classe de mensagens têm acesso a esses intervalos; uma propriedade com identificador _xxxx_ pode significar um comportamento para uma classe de mensagem e outro comportamento para outra classe de mensagem. 
  
As propriedades nomeadas são usadas para garantir que uma propriedade específica seja exclusiva para uma classe de mensagem. Os identificadores de propriedade nomeados começam no intervalo 0x8000. Os clientes definem um ou mais nomes e, em seguida, chamam o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) do repositório de mensagens para associar um identificador a cada nome. As propriedades nomeadas podem ser usadas por clientes ou provedores de serviços para definir novas propriedades para qualquer objeto somente se o proprietário do objeto suportar propriedades nomeadas. Os usuários dessas propriedades chamam **GetIDsFromNames** e um método **IMAPIProp** relacionado, [GetNamesFromIDs](imapiprop-getnamesfromids.md), para mapear entre um nome e seu identificador.
  
Todas as propriedades, nova ou existente, devem usar o conjunto de tipos de propriedade predefinido. Não é possível adicionar novos tipos de propriedade e os tipos existentes não podem ser modificados ou excluídos. Propriedades simples e pequenas, como as propriedades de um inteiro de caractere único ou de 16 bits, podem ser armazenadas em qualquer tipo apropriado. Por exemplo, inteiros podem ser armazenados como **ULONG** e as cadeias de caracteres podem ser armazenadas como **PT_STRING8**. 
  
Use o tipo **PT_BINARY** para indicar uma matriz de bytes contada. Esse tipo de propriedade é útil para estender os tipos de dados que podem ser armazenados em um objeto. Bytes são transmitidos em sequência e não são feitas suposições sobre o significado dos dados. Quando um aplicativo cliente lê dados de tal propriedade, os dados são inalterados de como foram armazenados. O cliente deve executar qualquer troca de bytes necessárias ao mover dados entre CPUs. 
  
## <a name="see-also"></a>Confira também



[Visão geral da propriedade MAPI](mapi-property-overview.md)

