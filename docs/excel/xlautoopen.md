---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- função xlAutoOpen [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765449"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de retorno de chamada que deve ser implementada e exportá-los por cada XLL válido. A função de **xlAutoOpen** é o local recomendado de onde para registrar funções e comandos XLL, inicializar estruturas de dados, personalize a interface do usuário e assim por diante. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A implementação dessa função deve retornar 1 (**int**).
  
## <a name="remarks"></a>Comentários

Microsoft Excel chama **xlAutoOpen** sempre que o XLL é ativado. XLL é ativado nas seguintes situações: 
  
- No início de uma sessão do Excel, caso este tenha sido ativa na última sessão Excel que terminou normalmente.
    
- Se carregado durante uma sessão do Excel.
    
- Um XLL pode ser carregado de várias maneiras:
    
- Escolhendo **Abrir** no menu **arquivo** (onde a versão do Excel oferece suporte a esse método de carregamento XLLs). 
    
- Usando o Gerenciador de Suplemento.
    
- A partir de outra XLL que chama [xlfRegister](xlfregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- De uma folha de macro XLM que chama [registrar](xlfregister-form-1.md) com o nome dessa DLL como o único argumento. 
    
- Se o suplemento é desativado e reativado durante uma sessão do Excel, essa função é chamada no reativação.
    
### <a name="example"></a>Exemplo

Consulte os arquivos `SAMPLES\EXAMPLE\EXAMPLE.C` e `SAMPLES\GENERIC\GENERIC.C`e por exemplo implementações dessa função.
  
## <a name="see-also"></a>Confira também



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

