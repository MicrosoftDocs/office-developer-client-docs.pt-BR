---
title: Implementar interface IUnknown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 01bba63b-a2a1-490e-8b78-5c9ba8d9547b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5165476ea131e40153191e8625af5ea3c49f47b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397412"
---
# <a name="implementing-the-iunknown-interface"></a>Implementar interface IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os métodos da interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) , implementado em cada objeto MAPI, suportam a gerenciamento de comunicação e o objeto interobject. 
  
 **IUnknown** possui três métodos: [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)e [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx). **QueryInterface** permite que um objeto para determinar se outro objeto suporta uma interface particular. Com **QueryInterface**, dois objetos sem conhecimento prévio da funcionalidade uns dos outros podem interagir. Se o objeto que implementa **QueryInterface** dá suporte a interface em questão, ele retorna um ponteiro para a implementação da interface. Se o objeto não suporta a interface solicitada, ele retornará o valor MAPI_E_INTERFACE_NOT_SUPPORTED. 
  
Quando **QueryInterface** retorna um ponteiro de interface solicitada, também deve aumentar contagem de referência do novo objeto. Contagem de referência de um objeto é um valor numérico usado para gerenciar o tempo de vida do objeto. Quando a contagem de referência for maior que 1, a memória do objeto não pode ser liberada porque ativamente está sendo usado. É somente quando a contagem de referência cai a 0 se o objeto pode ser liberado com segurança. 
  
Os outros dois **IUnknown** métodos, **AddRef** e **Release**, gerenciam a contagem de referência. **AddRef** incrementa a contagem de referência, enquanto diminui **versão** -lo. Todos os métodos ou funções da API que retornam ponteiros de interface, como **QueryInterface**, devem chamar **AddRef** para incrementar a contagem de referência. Todas as implementações dos métodos que recebem ponteiros de interface devem chamar **Release** para diminuir a contagem quando o ponteiro não é mais necessária. **Versão** verifica se há uma contagem de referência existente, dispensando a memória associada à interface somente se a contagem será 0. 
  
> [!NOTE]
> Porque **AddRef** e **Release** não são necessários para retornar valores precisos, os chamadores desses métodos não devem usar os valores de retorno para determinar se um objeto ainda é válido ou que tenha sido destruído. 
  
## <a name="see-also"></a>Confira também



[Implementar objetos MAPI](implementing-mapi-objects.md)

