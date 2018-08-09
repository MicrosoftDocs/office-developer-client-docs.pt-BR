---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Representa uma estrutura ACCT_BIN que contém o UID de uma conta do Exchange.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766080"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém o UID de uma conta do Exchange. 
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2009  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x20090102  <br/> |
|Access:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) para verificar se a conta é uma conta do Exchange. Se estiver, **PROP\_MAPI_EMSMDB_UID** é um **ACCT_BIN** que contém o **emsmdbUID**, que é a ID exclusiva, para a conta do Exchange. Se a conta não for uma conta do Exchange, essa propriedade é indefinida.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)
- [Usar várias contas do Exchange](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Propriedade canônica PidTagExchangeProfileSectionId](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

