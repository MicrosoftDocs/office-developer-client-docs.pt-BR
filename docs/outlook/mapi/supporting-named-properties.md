---
title: Suporte a propriedades nomeadas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770540"
---
# <a name="supporting-named-properties"></a>Suporte a propriedades nomeadas

  
  
**Aplica-se a**: Outlook 
  
Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties. Suporte a propriedades nomeadas é necessário para: 
  
- Provedores de catálogo de endereços que permitem entradas de outros provedores a serem copiados para seus contêineres.
    
- Provedores que podem ser usados para criar tipos de mensagem arbitrário de armazenamento de mensagem.
    
Propriedade nomeada suporte é opcional para todos os outros provedores de serviços. Provedores de serviço que oferecem suporte a propriedades nomeadas devem implementar o mapeamento de nome-para-identifier os métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Clientes chamadas **GetNamesFromIDs** para recuperar os nomes correspondentes para um ou mais identificadores de propriedade no intervalo 0x8000 failover e **GetIDsFromNames** criar ou recuperar os identificadores para um ou mais nomes. 
  
Provedores de serviços que não oferecem suporte a propriedades nomeadas devem:
  
- Transferir chamadas para [IMAPIProp::SetProps](imapiprop-setprops.md) para definir propriedades com identificadores de 0x8000 ou maior, retornando MAPI_E_UNEXPECTED_ID na matriz [SPropProblem](spropproblem.md) . 
    
- Retorne MAPI_E_NO_SUPPORT dos métodos [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) e [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
    

