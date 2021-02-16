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
description: Chama uma macro em um projeto do Microsoft Visual Basic for Applications (VBA).
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428085"
---
# <a name="runmacro-function"></a>Função RUNMACRO

Chama uma macro em um projeto do Microsoft Visual Basic for Applications (VBA). 
  
## <a name="syntax"></a>Sintaxe

RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da macro a ser chamada.  <br/> |
| _projname_opt_ <br/> |Opcional  <br/> |**String** <br/> | O projeto que contém a macro.  <br/> |
   
## <a name="remarks"></a>Comentários

Se um projeto for especificado, o Microsoft Visio verifica todos os documentos abertos em busca do que  _contém_ projname_opt e chama  _o nome da macro_ nesse projeto. Se  _projname_opt_ for omitido ou nulo (""), supõe-se que  _o nome da macro_ está no projeto VBA do documento que contém a fórmula RUNMACRO que está sendo avaliada. 
  
A função RUNMACRO difere da função CALLTHIS porque ela não passa uma referência à forma que possui a fórmula que está sendo avaliada para  _macroname_. Assim como CALLTHIS, a função RUNMACRO não exige uma referência projname_opt  _para_ chamá-la. 
  
 O código VBA, que é invocado quando a instância do Visio avalia uma função RUNMACRO em uma fórmula, não deve fechar o documento que contém a célula que está usando a função, uma vez que ocorrerá um erro de aplicativo e o Visio será fechado. 
  
Se você precisar fechar o documento que contém a célula que está utilizando a função RUNMACRO, utilize uma das técnicas a seguir:
  
- Feche o documento a partir de um código que não seja VBA.
    
- Feche o documento a partir de um projeto diferente do que está sendo fechado.
    
- Envie mensagens de janela para fechar as janelas em vez de fechar o documento.
    
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir invoca uma macro chamada MeuTeste no modelo de classe EsteDocumento do projeto VBA que contém a fórmula RUNMACRO. 
  
RUNMACRO ("EsteDocumento.MeuTeste") 
  

