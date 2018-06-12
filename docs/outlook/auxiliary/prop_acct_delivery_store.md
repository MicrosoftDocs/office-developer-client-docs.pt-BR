---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa a identificação de entrada do repositório de entrega padrão para a conta.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766048"
---
# <a name="propacctdeliverystore"></a>PROP_ACCT_DELIVERY_STORE

Representa a identificação de entrada do repositório de entrega padrão para a conta.
  
## <a name="quick-info"></a>Informações rápidas

Consulte [IOlkAccount](iolkaccount.md).
  
|||
|:-----|:-----|
|Identificador:  <br/> |0x0018  <br/> |
|Tipo de propriedade:  <br/> |PT_BINARY  <br/> |
|Marca de propriedade:  <br/> |0x00180102  <br/> |
|Access:  <br/> |Leitura/gravação  <br/> |
   
## <a name="remarks"></a>Coment�rios

Obter ou definir essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.
  
Um dos efeitos colaterais do definindo um repositório como repositório de entrega padrão para uma conta é que ao iniciar o Outlook, o Outlook cria as pastas de pesquisa para esse repositório se elas existirem e listar o repositório na barra de tarefas pendentes.
  
## <a name="see-also"></a>Confira também

- [Sobre a API de gerenciamento de conta](about-the-account-management-api.md)
- [Constantes (API de gerenciamento de conta)](constants-account-management-api.md)

