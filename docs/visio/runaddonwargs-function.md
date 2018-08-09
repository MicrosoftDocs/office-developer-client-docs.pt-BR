---
title: Função RUNADDONWARGS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251493
localization_priority: Normal
ms.assetid: c154413f-c366-a66b-94e3-ed71ad23f325
description: Executa a cadeia de caracteres e passa os argumentos de linha de comando para o programa como uma cadeia de caracteres.
ms.openlocfilehash: 7bc05a0cbf32550d1e39bee39bec83101882cf19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772831"
---
# <a name="runaddonwargs-function"></a>Função RUNADDONWARGS

Executa a _cadeia de caracteres_ e passa os _argumentos_ de linha de comando para o programa como uma cadeia de caracteres. 
  
## <a name="syntax"></a>Sintaxe

RUNADDONWARGS ("* * *cadeia de caracteres* * *","* * *argumentos* * *") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome de um complemento.  <br/> |
| _argumentos_ <br/> |Obrigatório  <br/> |**String** <br/> |Argumentos a serem passados para seu programa.  <br/> |
   
## <a name="remarks"></a>Comentários

Na prática, os _argumentos_ devem ser 50 caracteres ou menos. Use a função RUNADDONWARGS para vincular um programa, como um complemento, a uma célula, por exemplo, a uma célula Action ou Events. 
  
A função RUNADDONWARGS somente executa complementos que sejam membros da coleção **Addons** do aplicativo. Para fazer parte dessa coleção, um complemento precisar ser um arquivo EXE ou VSL, ou seja: 
  
- Instalado no caminho **Startup** ou **Addons** do aplicativo. 
    
- Adicionado de forma programática usando o método **Add** da coleção **Addons**. 
    
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
Em versões anteriores do Visio, essa função aparece como _RUNADDONWARGS. As versões 4.0 e posteriores do Visio aceitam os dois estilos.
  
## <a name="example"></a>Exemplo

RUNADDONWARGS ("GRAPHMKR. EXE"," / GraphMaker = Stack ") 
  
Iniciará o complemento Graphmkr.exe e passará o argumento /GraphMaker=Stack. 
  

