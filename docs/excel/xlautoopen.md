---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- Função xlautoopen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406644"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de retorno de chamada que deve ser implementada e exportada por cada XLL válido. A **função xlAutoOpen** é o local recomendado de onde registrar comandos e funções XLL, inicializar estruturas de dados, personalizar a interface do usuário e assim por diante. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Comentários

O Microsoft Excel **chama xlAutoOpen** sempre que o XLL é ativado. O XLL é ativado nas seguintes situações: 
  
- No início de uma sessão do Excel se ela estava ativa na última sessão do Excel que terminou normalmente.
    
- Se carregado durante uma sessão do Excel.
    
- Um XLL pode ser carregado de várias maneiras:
    
- Escolhendo **Abrir** no menu **Arquivo** (em que a versão do Excel dá suporte a esse método de carregamento de XLLs). 
    
- Usando o Gerenciador de Suplemento.
    
- De outro XLL que chama [xlfRegister](xlfregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- De uma folha de macro XLM que chama [REGISTER](xlfregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- Se o complemento for desativado e reativado durante uma sessão do Excel, essa função será chamada na reativação.
    
### <a name="example"></a>Exemplo

Consulte os arquivos  `SAMPLES\EXAMPLE\EXAMPLE.C`  `SAMPLES\GENERIC\GENERIC.C` e, por exemplo, implementações dessa função.
  
## <a name="see-also"></a>Confira também



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

