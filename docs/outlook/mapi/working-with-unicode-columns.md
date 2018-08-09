---
title: Trabalhar com colunas Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9f1fd2d4e4bfdc9ccbbb771fedf1141769c8c8ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770713"
---
# <a name="working-with-unicode-columns"></a>Trabalhar com colunas Unicode

  
  
**Aplica-se a**: Outlook 
  
Cadeias de caracteres nas tabelas podem ser representadas usando caracteres padrão de 8 bits, que são o tipo de propriedade PT_STRING8, ou caracteres Unicode de 16 bits, que são do tipo de propriedade PT_UNICODE. Implementadores de tabela são livres para escolher se ou não suas tabelas suportam a cadeias de caracteres Unicode. Como Unicode adiciona o valor para clientes e provedores de serviços, estendendo o conjunto de recursos, recomenda-se o suporte a Unicode sempre que possível. 
  
Muitos métodos de tabela aceitam um sinalizador que determina se ou não os valores de propriedade de cadeia de caracteres esperados Unicode. Na entrada, especificar o sinalizador MAPI_UNICODE indica o implementador da tabela que todos os valores de propriedade de cadeia de caracteres passados com a chamada são cadeias de caracteres Unicode e tem tipos de propriedade de PT_UNICODE. Na saída, esse sinalizador indica que todos os valores de propriedade de cadeia de caracteres retornada devem ser cadeias de caracteres Unicode, se possível. Se o sinalizador tem um significado para entrada ou saída depende do método. Implementadores de tabela que não oferecem suporte a Unicode e são passados o sinalizador MAPI_UNICODE retornam o valor MAPI_E_BAD_CHAR_WIDTH.
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)
