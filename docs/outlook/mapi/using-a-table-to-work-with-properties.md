---
title: Usando uma tabela para trabalhar com propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 59196f136c422be912ac2460cbbd25d8bc2e3330
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439909"
---
# <a name="using-a-table-to-work-with-properties"></a>Usando uma tabela para trabalhar com propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Muitas propriedades estão disponíveis nos objetos que as suportam e como colunas em tabelas. Sempre que possível, recupere essas propriedades por meio da tabela.
  
Chame [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas as propriedades de que seu cliente precisa e [IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela. 
  
Essas duas chamadas geralmente são suficientes para recuperar informações suficientes para exibição para um usuário e são frequentemente suficientes para qualquer processamento interno necessário, fazendo uma chamada para **OpenEntry** para abrir o objeto desnecessária. 
  
Há apenas duas exceções:
  
- Se a propriedade for maior que 255 bytes. A interface ** IMAPITable ** pode não retornar o valor inteiro da propriedade, truncando-a em 255 bytes. Porém, pense nessa troca. Se você estiver exibindo esses dados para o usuário, 255 bytes podem ser suficientes para um campo textual, como um comentário. 
    
- Se você precisar de uma propriedade específica de uma única linha em uma tabela. Nesse caso, não é necessário criar uma tabela com propriedades que nunca serão usadas. Na maioria das vezes, você precisará das mesmas propriedades para todas as linhas.
    

