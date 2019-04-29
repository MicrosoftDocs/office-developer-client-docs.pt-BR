---
title: Função DECIMALSEP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Retorna a cadeia de caracteres do separador decimal para a localidade do usuário atual.
ms.openlocfilehash: 8a59e7331fd51cf5426b5e2cdd64e3c5a22334b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360302"
---
# <a name="decimalsep-function"></a>Função DECIMALSEP

Retorna a cadeia de caracteres do separador decimal para a localidade do usuário atual.
  
## <a name="syntax"></a>Sintaxe

DECIMALSEP( )
  
## <a name="example"></a>Exemplo

SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart) 
  

