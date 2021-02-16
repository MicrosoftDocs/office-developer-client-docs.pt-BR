---
title: Trabalhando com colunas Unicode
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2cd55464-263f-4f83-b874-524271773934
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 76d1afb750dc81b889ca8e5eb3639145c061bfc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408380"
---
# <a name="working-with-unicode-columns"></a>Trabalhando com colunas Unicode

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cadeias de caracteres em tabelas podem ser representadas usando caracteres padrão de 8 bits, que são caracteres do tipo PT_STRING8 ou caracteres Unicode de 16 bits, que são tipos de propriedade PT_UNICODE. Implementadores de tabela são livres para escolher se suas tabelas suportam ou não cadeias de caracteres Unicode. Como Unicode adiciona valor para clientes e provedores de serviços estendendo o conjunto de recursos, é recomendável oferecer suporte a Unicode sempre que possível. 
  
Muitos métodos de tabela aceitam um sinalizador que determina se os valores de propriedade de cadeia de caracteres devem ou não ser Unicode. Na entrada, especificar o sinalizador MAPI_UNICODE indica ao implementador de tabela que todos os valores de propriedade de cadeia de caracteres passados com a chamada são cadeias de caracteres Unicode e têm tipos de propriedade PT_UNICODE. Na saída, esse sinalizador indica que todos os valores de propriedade de cadeia de caracteres retornados devem ser cadeias de caracteres Unicode, se possível. Se o sinalizador tem um significado para entrada ou saída depende do método. Implementadores de tabela que não suportam Unicode e são passados o sinalizador MAPI_UNICODE retornam o MAPI_E_BAD_CHAR_WIDTH valor.
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

