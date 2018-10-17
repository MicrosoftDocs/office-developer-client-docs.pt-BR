---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Representa uma estrutura ACCT_BIN que contém a UID de uma conta do Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395277"
---
# <a name="propmapiemsmdbuid"></a>PROP_MAPI_EMSMDB_UID

Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém a UID de uma conta do Exchange. 
  
## <a name="quick-info"></a>Informações rápidas

Confira [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x2009  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x20090102  <br/> |
|Acesso:  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).
  
Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) para verificar se a conta é uma conta do Exchange. Se for, **PROP\_MAPI_EMSMDB_UID** será um **ACCT_BIN** que contém a **emsmdbUID**, que é a ID exclusiva da conta do Exchange. Se a conta não for do Exchange, essa propriedade ficará indefinida.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de contas](about-the-account-management-api.md) 
- [Constantes (API de gerenciamento de contas)](constants-account-management-api.md)
- [Usar várias contas do Exchange](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [Propriedade canônica PidTagExchangeProfileSectionId](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

