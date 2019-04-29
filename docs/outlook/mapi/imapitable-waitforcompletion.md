---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407057"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Suspende o processamento até que uma ou mais operações assíncronas em andamento na tabela tenham sido concluídas.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> Serve deve ser zero.
    
 _ulTimeout_
  
> no Número máximo de milissegundos para aguardar a conclusão da operação ou operações assíncronas. Para esperar indefinidamente até a conclusão ocorrer, defina _ulTimeout_ como 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [in, out] Na entrada, um ponteiro válido ou nulo. Na saída, se _lpulTableStatus_ for um ponteiro válido, apontará para o status mais recente da tabela. Se _lpulTableStatus_ for NULL, nenhuma informação de status será retornada. Se **WaitForCompletion** retornar um valor de HRESULT sem êxito, o conteúdo de _lpulTableStatus_ será indefinido. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A operação de espera foi bem-sucedida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não dá suporte à espera para a conclusão de operações assíncronas.
    
MAPI_E_TIMEOUT 
  
> A operação assíncrona ou as operações não foram concluídas no tempo especificado.
    
## <a name="remarks"></a>Comentários

O método imApitable **:: WaitForCompletion** suspende o processamento até que qualquer operação assíncrona atualmente em andamento para a tabela tenha sido concluída. **WaitForCompletion** pode permitir que as operações assíncronas sejam totalmente concluídas ou sejam executadas por um determinado número de milissegundos, conforme indicado por _ulTimeout_, antes de ser interrompido. Para detectar operações assíncronas em andamento, chame o método imApitable [:: GetStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

