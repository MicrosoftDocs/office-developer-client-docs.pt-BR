---
title: Excel XLL SDK API Function Reference
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715953"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Excel XLL SDK API Function Reference

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O SDK do Microsoft Excel 2013 XLL contém arquivos de origem para uma biblioteca do Framework que é projetada para acelerar a gravação de XLLs e dois exemplos de projetos, Exemplo e Genérico. 
  
Esta seção fornece uma referência de função para o seguinte:
  
- Retornos de chamada do Excel que o XLL pode chamar.
    
- Retornos de chamada do XLL que o Microsoft Excel procura.
    
- Principais funções nas estruturas e projetos de exemplo.
    
## <a name="sample-projects"></a>Projetos de exemplo

O SDK do Excel 2013 XLL fornece arquivos de origem e arquivos de projeto do Microsoft Visual Studio para os seguintes projetos de exemplo:
  
- O projeto do **Framework** (`SAMPLES\FRAMEWRK\`) contém um projeto que pode ser criado em uma biblioteca, FRAMEWRK.lib, que pode ser vinculado a outros projetos do XLL. A biblioteca contém muitas funções e ferramentas para facilitar a gravação de XLLs. Essa biblioteca é usada nos outros dois projetos juntamente com o arquivo de cabeçalho FRAMEWRK.h.
    
- O projeto de **Exemplo** (`SAMPLES\EXAMPLE\`) contém um projeto que pode ser criado para um XLL, EXAMPLE.xll. O XLL contém muitos exemplos do uso da biblioteca do Framework e exemplos de implementações das funções de interface do suplemento XLL, como **xlAutoOpen**.
    
- O projeto de **Genérico** (`SAMPLES\GENERIC\`) contém um projeto que pode ser criado para um XLL, GENERIC.xll. O XLL demonstra várias funções e comandos de exemplo e é um bom ponto de partida para gravar seus próprios XLLs.
    
## <a name="in-this-section"></a>Nesta seção

- [Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)
  
- [Retorno de chamada da API de C: funções Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)
  
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Funções na biblioteca do Framework](functions-in-the-framework-library.md)
  
- [Funções na DLL genérica](functions-in-the-generic-dll.md)
  
- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Confira também

- [Programação com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

