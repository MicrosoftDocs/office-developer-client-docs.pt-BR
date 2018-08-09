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
ms.openlocfilehash: e425dd9605c18d4647787c5df7aeaa4fd5f9e4cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771737"
---
# <a name="docmd-function"></a>Função DOCMD

Executa o comando identificado.
  
## <a name="syntax"></a>Sintaxe

 **DOCMD** ( _ID de comando_)
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ID de comando_ <br/> |Obrigatório  <br/> |**Número** <br/> | O comando a ser executado.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter uma lista de comandos que são compatíveis com a função DOCMD, consulte o tópico "Comandos DoCmd/DOCMD" na referência de automação do Microsoft Visio 2013. 
  
## <a name="example"></a>Exemplo

 `DOCMD (1312)`
  
Faz com que a caixa de diálogo **Dados da Forma** seja exibida na interface do usuário. 
  

