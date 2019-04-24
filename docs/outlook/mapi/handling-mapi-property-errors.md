---
title: Manipular erros de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1dc676101d4c39544c9dd1fae94000db9963ea02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299382"
---
# <a name="handling-mapi-property-errors"></a>Manipular erros de propriedade MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Em vez de falha completa ou sucesso, os seguintes m�todos de **IMAPIProp** relatar �xito parcial: 
  
[GetProps](imapiprop-getprops.md)
  
[SetProps](imapiprop-setprops.md)
  
[DeleteProps](imapiprop-deleteprops.md)
  
[CopyTo](imapiprop-copyto.md)
  
[CopyProps](imapiprop-copyprops.md)
  
**GetProps** relat�rios sucesso parcial quando ele pode recuperar pelo menos uma das propriedades solicitadas para um objeto. **GetProps** indica �xito parcial, retornando o aviso MAPI_W_ERRORS_RETURNED e colocando informa��es sobre as propriedades n�o est� dispon�veis da matriz de valores de propriedade apontado pelo par�metro **lppPropArray**. Entrada de uma propriedade n�o est� dispon�vel nessa matriz cont�m PT_ERROR para o tipo de propriedade no membro do **ulPropTag** e E_NOT_FOUND ou outro valor de erro apropriado para o membro **Value**. Por exemplo, se um cliente chama o m�todo de **GetProps** de uma pasta para recuperar tr�s propriedades e a terceira n�o estiver dispon�vel, o provedor de armazenamento de mensagem coloca PT_ERROR no terceiro tipo de propriedade da matriz de valores de propriedade e E_NOT_FOUND no valor da propriedade terceiro. 
  
Outros m�todos **IMAPIProp** relatar �xito parcial de forma diferente. Esses m�todos relatar �xito parcial, retornando S_OK e colocando informa��es de erro em uma estrutura [SPropProblemArray](spropproblemarray.md) . Ao contr�rio de matriz de valores de propriedade em **GetProps** que cont�m dados independentemente se o m�todo teve �xito ou falha, a matriz de problema da propriedade nesses m�todos existe somente se h� erros e somente se o chamador registrou interesse em saber mais sobre os erros. Os chamadores devem especificar um ponteiro v�lido **SPropProblemArray** para registrar para obter informa��es de erro. 
  
Quando um valor de erro � retornado de **SetProps**, **DeleteProps**, **CopyTo**ou **CopyProps**, isto indica falha em vez de sucesso parcial. A matriz de problema de propriedade, se estiver dispon�vel, n�o � v�lida. Os clientes n�o devem tentar acessar dados mantidos na estrutura nem deve tentar liberar a estrutura em si. A resposta apropriada � chamar [IMAPIProp::GetLastError](imapiprop-getlasterror.md). 
  
**GetLastError** � semelhante � fun��o do mesmo nome fornecido no SDK do Windows. Ambos fornecem que informa��es mais detalhadas sobre um erro que est� dispon�vel com o valor de retorno. Ambos retornarem informa��es sobre o erro anterior que tenha ocorrido. A diferen�a � que a fun��o de **GetLastError** Win32 relat�rios sobre um erro gerado pelo thread de chamada e o m�todo **IMAPIProp::GetLastError** relat�rios sobre um erro gerado pelo objeto atual. Ou seja, se um cliente chama **DeleteProps** em uma mensagem e MAPI_E_NO_ACCESS � retornado para indicar que a mensagem � somente leitura, **GetLastError** retorna dados fornecidos pela mensagem. 
  
## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

