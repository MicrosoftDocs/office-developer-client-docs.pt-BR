---
title: Função FIND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Localiza uma cadeia de texto contida na outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de texto que você está procurando em relação à sua posição na cadeia de texto que o contém.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771905"
---
# <a name="find-function"></a>Função FIND

Localiza uma cadeia de texto contida na outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de texto que você está procurando em relação à sua posição na cadeia de texto que o contém.
  
## <a name="syntax"></a>Sintaxe

ENCONTRE (* * *texto_procurado* * *, * * *No_texto* * *, [* * *Núm_inicial* * *], [* * *ignore_case* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _texto_procurado_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres de texto a ser localizada.  <br/> |
| _format_ <br/> |Obrigatório  <br/> |**String** <br/> |A cadeia de caracteres que contém o texto a ser localizado.  <br/> |
| _Núm_inicial_ <br/> |Opcional  <br/> |**Número** <br/> |O caractere a partir do qual iniciar a pesquisa. O primeiro caractere em _No_texto_ é 1. Se _Núm_inicial_ estiver ausente, será considerado como 1.  <br/> |
| _ignore_case_ <br/> |Opcional  <br/> |**Boolean** <br/> |Por padrão, a função FIND distingue maiúsculas e minúsculas. Para que a função FIND ignore maiúsculas e minúsculas, defina este argumento como TRUE.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

Se várias correspondências forem encontradas, a função Localizar retorna a posição inicial da primeira correspondência na cadeia de caracteres. O argumento _texto_procurado_ não considera qualquer caractere como curinga. 
  
Se _texto_procurado_:
  
-  Estiver vazio (""), procurar coincide com o primeiro caractere na sequência de pesquisa (ou seja, o caractere numerado _Núm_inicial_ ou 1). 
    
- Não aparece em _within_text_, FIND retornará o #VALUE! valor de erro. 
    
Se _Núm_inicial_:
  
- Não for maior que zero (0), FIND retornará o valor de erro #VALUE! 
    
- É maior que o comprimento de _No_texto_, Find retornará o #VALUE! valor de erro. 
    
## <a name="example"></a>Exemplo

FIND ("2003","1º de janeiro de 2003") 
  
Retornará 12. 
  

