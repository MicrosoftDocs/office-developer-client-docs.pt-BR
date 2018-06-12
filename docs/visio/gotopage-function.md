---
title: Função GOTOPAGE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Exibe a página que tenha o pagename nome na janela ativa no momento.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771986"
---
# <a name="gotopage-function"></a>Função GOTOPAGE

Exibe a página que tem o nome *pagename* na janela ativa no momento. 
  
## <a name="syntax"></a>Sintaxe

GOTOPAGE ("* * *pagename* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da página a ser acessada.  <br/> |
   
## <a name="remarks"></a>Comentários

Se uma janela já estiver exibindo a página, essa janela ficará ativa. Se *pagename* não existir, o aplicativo tenta navegue até http:// *pagename* /. Se o Visio estiver agindo como um servidor in-loco, a função GOTOPAGE não terá efeito. 
  
É possível utilizar a função HYPERLINK para navegar por qualquer caminho DOS, UNC ou URL. 
  
Em versões anteriores dos produtos Visio, essa função aparece como _GOTOPAGE. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  

