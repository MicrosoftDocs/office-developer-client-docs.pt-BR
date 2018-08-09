---
title: Função RUNMACRO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Chama uma macro em um Microsoft Visual Basic para o project Applications (VBA).
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772832"
---
# <a name="runmacro-function"></a>Função RUNMACRO

Chama uma macro em um Microsoft Visual Basic para o project Applications (VBA). 
  
## <a name="syntax"></a>Sintaxe

RUNMACRO (* * *macroname* * * [, * * *nomeProj_opc* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da macro a ser chamada.  <br/> |
| _nomeProj_opc_ <br/> |Opcional  <br/> |**String** <br/> | O projeto que contém a macro.  <br/> |
   
## <a name="remarks"></a>Comentários

Se um projeto for especificado, o Microsoft Visio verifica todos os documentos abertos para a um que contêm chamadas e _nomeProj_opc_ _macroname_ no projeto. Se _nomeProj_opc_ for omitido ou nulo (""), _macroname_ será considerado no projeto VBA do documento que contém a fórmula RUNMACRO sendo avaliada. 
  
A função RUNMACRO difere da função CALLTHIS não passe uma referência para a forma que contém a fórmula sendo avaliada para _macroname_. Assim como CALLTHIS, a função RUNMACRO não exige uma referência para _nomeProj_opc_ para ligar para ele. 
  
 O código VBA, que é invocado quando a instância do Visio avalia uma função RUNMACRO em uma fórmula, não deve fechar o documento que contém a célula que está usando a função, uma vez que ocorrerá um erro de aplicativo e o Visio será fechado. 
  
Se você precisar fechar o documento que contém a célula que está utilizando a função RUNMACRO, utilize uma das técnicas a seguir:
  
- Feche o documento a partir de um código que não seja VBA.
    
- Feche o documento a partir de um projeto diferente do que está sendo fechado.
    
- Envie mensagens de janela para fechar as janelas em vez de fechar o documento.
    
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir invoca uma macro chamada MeuTeste no modelo de classe EsteDocumento do projeto VBA que contém a fórmula RUNMACRO. 
  
RUNMACRO ("EsteDocumento.MeuTeste") 
  

