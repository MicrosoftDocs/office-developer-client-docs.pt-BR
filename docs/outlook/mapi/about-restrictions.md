---
title: Sobre restrições
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e119fa20-08b8-4c8d-93fc-56037220890d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 139526937380273703a96f91f2bae02a79debc76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433105"
---
# <a name="about-restrictions"></a>Sobre restrições

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma restrição é uma maneira de limitar o número de linhas em um modo de exibição apenas às linhas com valores para colunas que correspondem a critérios específicos. Há várias oportunidades diferentes de usar restrições com tabelas. Os aplicativos cliente podem usar restrições, por exemplo, para filtrar uma tabela de conteúdo para mensagens enviadas por uma determinada pessoa, procurar linhas que não dão suporte a uma propriedade ou definir uma propriedade para um valor específico ou procurar destinatários duplicados em um Mensagem. 
  
Os métodos imApitable: [: Restrict](imapitable-restrict.md) e IMAPITable [:: FindRow](imapitable-findrow.md) são usados para definir restrições em uma tabela. **Restrict** aplica a restrição à tabela sem recuperar nenhuma linha. Para recuperar apenas as linhas que atendem à restrição, uma chamada subsequente para imApitable [:: QueryRows](imapitable-queryrows.md) ou um método semelhante é necessária. **FindRow** aplica a restrição e recupera a primeira linha na tabela que corresponde aos critérios. **FindRow** aplica uma restrição temporária, que está em existência somente pela duração da chamada, enquanto restrict **** aplica uma restrição mais permanente. 
  
Alguns clientes podem criar uma restrição usando colunas que não estão no conjunto de colunas atual. O suporte a uma restrição é opcional e os implementadores de tabela que suportam o valor agregado, especialmente para tabelas de conteúdo. Os implementadores de tabela que não oferecem suporte a ele podem retornar o valor MAPI_E_TOO_COMPLEX de uma chamada **restrita** ou o valor de MAPI_E_NOT_FOUND de uma chamada **FindRow** . 
  
Os clientes devem estar cientes de que, mesmo que o provedor não tenha restrições de suporte em colunas que não estejam no conjunto de colunas atual, eles terão um desempenho melhor, especificando as colunas que pretendem usar em suas restrições com imApitable [::](imapitable-setcolumns.md) SetColumns .
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

