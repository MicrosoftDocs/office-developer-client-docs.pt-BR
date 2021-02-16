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
description: Executa a cadeia de caracteres e passa os argumentos da linha de comando para o programa como uma cadeia de caracteres.
ms.openlocfilehash: bc05a4480438875c348373059f57bf04f82c9eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408702"
---
# <a name="runaddonwargs-function"></a>Função RUNADDONWARGS

Executa  _a cadeia_ de caracteres e passa os  _argumentos da_ linha de comando para o programa como uma cadeia de caracteres. 
  
## <a name="syntax"></a>Sintaxe

RUNADDONWARGS(" ** *string* ** "," ** *arguments* ** ") 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome de um complemento.  <br/> |
| _arguments_ <br/> |Obrigatório  <br/> |**String** <br/> |Argumentos a serem passados para seu programa.  <br/> |
   
## <a name="remarks"></a>Comentários

Na prática,  _os argumentos devem_ ter 50 caracteres ou menos. Utilize a função RUNADDONWARGS para vincular um programa, como um complemento, a uma célula, por exemplo Action ou Events. 
  
A função RUNADDONWARGS somente executa complementos que sejam membros da coleção **Addons** do aplicativo. Para fazer parte dessa coleção, um complemento precisar ser um arquivo EXE ou VSL, ou seja: 
  
- Instalado no caminho **Startup** ou **Addons** do aplicativo. 
    
- Adicionado de forma programática usando o método **Add** da coleção **Addons**. 
    
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
Em versões anteriores do Visio, essa função aparece como _RUNADDONWARGS. As versões 4.0 e posteriores do Visio aceitam os dois estilos.
  
## <a name="example"></a>Exemplo

RUNADDONWARGS("GRAPHMKR.EXE","/GraphMaker=Stack") 
  
Iniciará o complemento Graphmkr.exe e passará o argumento /GraphMaker=Stack. 
  

