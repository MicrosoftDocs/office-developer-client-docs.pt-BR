---
title: Função DOCMD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Executa o comando identificado.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315229"
---
# <a name="docmd-function"></a>Função DOCMD

Executa o comando identificado.
  
## <a name="syntax"></a>Sintaxe

 **DoCmd** ( _commandID_)
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Obrigatório  <br/> |**Número** <br/> | O comando a ser executado.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma lista de comandos que são compatíveis com a função DOCMD, consulte o tópico "comandos DoCmd/DOCMD" na referência de automação do Microsoft Visio 2013. 
  
## <a name="example"></a>Exemplo

 `DOCMD (1312)`
  
Faz com que a caixa de diálogo **Dados da Forma** seja exibida na interface do usuário. 
  

