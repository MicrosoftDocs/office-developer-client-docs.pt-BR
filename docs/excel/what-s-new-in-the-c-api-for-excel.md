---
title: Quais são as novidades na API de C para o Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- API de c [Excel 2007], o que há de novo
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310266"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Quais são as novidades na API de C para o Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Em conjunto com o Microsoft Excel 2013, o Microsoft Excel 2013 XLL Software Development Kit (SDK) inclui suporte para os seguintes recursos.
  
- **Novas funções**
    
    O Microsoft Excel 2013 XLL SDK oferece suporte à chamada de retorno a todas as novas funções de planilha do Excel 2013. Para obter mais informações sobre como chamar funções do Excel 2013, consulte ligando-se [ao Excel da dll ou XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Funções asSíncronas definidas pelo usuário**
    
    O Excel 2013 oferece suporte à chamada de funções definidas pelo usuário (UDF) de forma assíncrona, o que pode melhorar o desempenho, permitindo que vários cálculos sejam executados ao mesmo tempo. Para obter mais informações sobre UDFs assíncronos, consulte [funções assíncronas definidas pelo usuário](asynchronous-user-defined-functions.md).
    
- **Conectores de cluster**
    
    Os conectores de cluster permitem que os UDFs sejam executados em clusters de computação de alto desempenho. Para obter mais informações sobre a criação de conectores de cluster, consulte desenvolvimento de conectores de [cluster do Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Os suplementos XLL que você pretende executar em clusters de computação devem chamar apenas funções com segurança de cluster. Para obter mais informações sobre as funções que você pode usar, confira [referência de função da API do SDK XLL do Excel](excel-xll-sdk-api-function-reference.md) e [funções seguras de cluster](cluster-safe-functions.md). 
  
- **Suporte de 64 bits**
    
    Agora você pode compilar e vincular os XLLs de 32 bits e 64 bits. Para obter mais informações, consulte [Creating XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Confira também



[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Programação com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
[Multithreading e conTenção de memória no Excel](multithreading-and-memory-contention-in-excel.md)


[Introdução ao Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

