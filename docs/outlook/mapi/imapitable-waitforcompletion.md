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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c7859e033924786e415f9faa9f75021ea47968c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767346"
---
# <a name="imapitablewaitforcompletion"></a>IMAPITable::WaitForCompletion

  
  
**Aplica-se a**: Outlook 
  
Suspende o processamento até que um ou mais operações assíncronas em andamento na tabela forem concluídas.
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> Reservado; deve ser zero.
    
 _ulTimeout_
  
> [in] Número máximo de milissegundos de espera para a operação assíncrona ou a conclusão das operações. Para esperar indefinidamente até que ocorra de conclusão, defina _ulTimeout_ como 0xFFFFFFFF. 
    
 _lpulTableStatus_
  
> [além, out] Na entrada, um ponteiro válido ou nulo. Na saída, se _lpulTableStatus_ for um ponteiro válido, ela aponta para o status mais recente da tabela. Se _lpulTableStatus_ for NULL, nenhuma informação de status será retornada. Se **WaitForCompletion** retorna um valor HRESULT bem sucedido, o conteúdo de _lpulTableStatus_ é indefinido. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A operação de espera foi bem-sucedida.
    
MAPI_E_NO_SUPPORT 
  
> A tabela não oferece suporte ao aguardar a conclusão de operações assíncronas.
    
MAPI_E_TIMEOUT 
  
> A operação assíncrona ou operações não foram concluída no tempo especificado.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPITable::WaitForCompletion** suspende o processamento até que tenha concluído a qualquer operação assíncrona em andamento no momento para a tabela. **WaitForCompletion** pode permitir que as operações assíncronas para totalmente concluída ou a ser executada para um determinado número de milissegundos, conforme indicado pela _ulTimeout_, antes da interrupção. Para detectar operações assíncronas em andamento, chame o método [IMAPITable::GetStatus](imapitable-getstatus.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::GetStatus](imapitable-getstatus.md)
  
[IMAPITable:: Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable:: SortTable](imapitable-sorttable.md)
  
[IMAPITable: IUnknown](imapitableiunknown.md)

