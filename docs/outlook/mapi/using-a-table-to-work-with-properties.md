---
title: Usar uma tabela para trabalhar com propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c18ed9f7-c053-4453-b0b1-06234cdfb025
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e4e7ecda40f3f3fcb05700ba3e8b79ab21cbe35b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770681"
---
# <a name="using-a-table-to-work-with-properties"></a>Usar uma tabela para trabalhar com propriedades

  
  
**Aplica-se a**: Outlook 
  
Muitas propriedades estão disponíveis nos objetos que dão suporte a eles e como colunas nas tabelas. Sempre que possível, recupere essas propriedades por meio da tabela.
  
Chamadas [IMAPITable::SetColumns](imapitable-setcolumns.md) para incluir todas as propriedades que precisa de seu cliente e [IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar todas as linhas da tabela. 
  
Essas duas chamadas geralmente são suficientes para recuperar informações suficientes para exibir a um usuário e são frequentemente suficientes para qualquer processamento interno necessário, fazendo uma chamada para **OpenEntry** para abrir o objeto desnecessário. 
  
Existem apenas duas exceções:
  
- Se a propriedade for com mais de 255 bytes. O * * IMAPITable * * interface não pode retornar o valor da propriedade inteira, em vez disso, truncá-la em 255 bytes. Pense essa compensação, no entanto. Se você estiver exibindo esses dados para o usuário, 255 bytes pode ser suficiente para que um campo textual como um comentário. 
    
- Se você precisa de uma propriedade específica de uma única linha em uma tabela. Nesse caso é desnecessário criar uma tabela com propriedades que nunca serão usadas. Na maioria das vezes você precisará as mesmas propriedades para todas as linhas.
    

