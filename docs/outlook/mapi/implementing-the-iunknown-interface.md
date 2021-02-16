---
title: Implementando a interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310042"
---
# <a name="implementing-the-iunknown-interface"></a>Implementando a interface IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os métodos da interface [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) implementados em cada objeto MAPI, suportam comunicação interobjeto e gerenciamento de objetos. 
  
 **IUnknown** tem três métodos: [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** permite que um objeto determine se outro objeto oferece suporte a uma interface específica. Com **QueryInterface**, dois objetos sem conhecimento prévio sobre a funcionalidade uns dos outros podem interagir. Se o objeto que implementa **QueryInterface** suporta a interface em questão, ele retorna um ponteiro para a implementação da interface. Se o objeto não suportar a interface solicitada, ele retornará o MAPI_E_INTERFACE_NOT_SUPPORTED valor. 
  
Quando **QueryInterface** retorna um ponteiro de interface solicitado, ele também deve aumentar a contagem de referência do novo objeto. A contagem de referência de um objeto é um valor numérico usado para gerenciar o tempo de vida do objeto. Quando a contagem de referência é maior que 1, a memória do objeto não pode ser liberada porque está sendo usada ativamente. É apenas quando a contagem de referência cai para 0 que o objeto pode ser liberado com segurança. 
  
Os outros dois **métodos IUnknown,** **AddRef** e **Release,** gerenciam a contagem de referência. **AddRef** incrementa a contagem de referência, enquanto **Release** a diminui. Todos os métodos ou funções de API que retornam ponteiros de interface, como **QueryInterface,** devem chamar **AddRef** para incrementar a contagem de referência. Todas as implementações de métodos que recebem ponteiros de interface devem chamar **Release** para rebaixar a contagem quando o ponteiro não for mais necessário. **Verificações** de versão para uma contagem de referência existente, liberando a memória associada à interface somente se a contagem for 0. 
  
> [!NOTE]
> Como **AddRef** e **Release** não são necessários para retornar valores precisos, os chamadores desses métodos não devem usar os valores de retorno para determinar se um objeto ainda é válido ou foi destruído. 
  
## <a name="see-also"></a>Confira também



[Implementando objetos MAPI](implementing-mapi-objects.md)

