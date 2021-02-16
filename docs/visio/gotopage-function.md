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
description: Exibe a página que tem o nome pagename na janela ativa no momento.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302965"
---
# <a name="gotopage-function"></a>Função GOTOPAGE

Exibe a página que tem o nome  *pagename*  na janela ativa no momento. 
  
## <a name="syntax"></a>Sintaxe

GOTOPAGE(" ** *pagename* ** ") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da página a ser acessada.  <br/> |
   
## <a name="remarks"></a>Comentários

Se uma janela já estiver exibindo a página, essa janela ficará ativa. Se  *o nome da*  página não existir, o aplicativo tentará navegar até https://  *pagename*  /. Se o Visio estiver agindo como um servidor in-loco, a função GOTOPAGE não terá nenhum efeito. 
  
É possível utilizar a função HYPERLINK para navegar por qualquer caminho DOS, UNC ou URL. 
  
Em versões anteriores dos produtos Visio, essa função aparece como _GOTOPAGE. As versões 4.0 e posteriores do Visio aceitam os dois estilos. 
  

