---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348367"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona ou move colunas no início de uma tabela existente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a>Parâmetros

 _lptbl_
  
> no Ponteiro para a tabela MAPI afetada. 
    
 _lpproptagColumnsNew_
  
> no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade para as propriedades a serem adicionadas ou movidas para o início da tabela. 
    
 _lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
 _lpfnFilterColumns_
  
> no Ponteiro para uma função de retorno de chamada fornecida pelo chamador. Se o parâmetro _lpfnFilterColumns_ estiver definido como nulo, nenhum retorno de chamada será feito. 
    
 _ptaga_
  
> no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém a matriz de marcas de propriedade já existentes na tabela antes das propriedades serem adicionadas ou movidas para o início. **HrAddColumnsEx** passa esse ponteiro como o parâmetro para a função de retorno de chamada indicada por _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e as colunas especificadas foram movidas ou adicionadas.
    
## <a name="remarks"></a>Comentários

As propriedades passadas para **HrAddColumnsEx** usando o parâmetro _lpproptagColumnsNew_ se tornam as primeiras propriedades expostas em chamadas subsequentes para o método IMAPITable [:: QueryRows](imapitable-queryrows.md) . Quaisquer propriedades anteriormente na tabela que não foram especificadas no parâmetro _lpproptagColumnsNew_ são expostas após todas as propriedades adicionadas e movidas. 
  
Se qualquer propriedade da tabela estiver indefinida quando **QueryRows** for chamado, elas serão retornadas com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrAddColumnsEx** permite que o chamador forneça uma função de retorno de chamada para filtrar as colunas que já estavam na tabela, por exemplo, para converter cadeias de caracteres do tipo de propriedade PT_UNICODE para PT_STRING8. **HrAddColumnsEx** passa um ponteiro para o conjunto de colunas existente anteriormente como o parâmetro para a função de retorno de chamada. A função de retorno de chamada pode alterar os dados na matriz de marca de propriedade, mas não pode adicionar novas marcas. 
  
 **HrAddColumnsEx** primeiro chama a função de retorno de chamada, se uma for fornecida, adiciona ou move as colunas especificadas e, finalmente, chama IMAPITable [::](imapitable-setcolumns.md)SetColumns. 
  
Os parâmetros de entrada _lpAllocateBuffer_ e _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Os valores exatos dos ponteiros passados para **HrAddColumnsEx** dependem do fato de o chamador ser um aplicativo cliente ou um provedor de serviços. Um cliente passa ponteiros para as funções MAPI com os nomes especificados. Um provedor de serviços passa os ponteiros recebidos em sua chamada de inicialização ou recuperados chamando o método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

