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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766765"
---
# <a name="hraddcolumnsex"></a>HrAddColumnsEx

  
  
**Aplica-se a**: Outlook 
  
Adiciona ou move colunas para o início de uma tabela existente. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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

## <a name="parameters"></a>Par�metros

 _lptbl_
  
> [in] Ponteiro para a tabela MAPI afetado. 
    
 _lpproptagColumnsNew_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade para as propriedades sejam adicionados ou movidos para o início da tabela. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _lpfnFilterColumns_
  
> [in] Ponteiro para uma função de retorno de chamada fornecido pelo chamador. Se o parâmetro _lpfnFilterColumns_ for definido como NULL, sem retorno de chamada é estabelecido. 
    
 _ptaga_
  
> [in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém a matriz de marcas de propriedade já existentes na tabela antes de propriedades são adicionadas ou movidas para o início. Passa de **HrAddColumnsEx** esse ponteiro como o parâmetro para a função de retorno de chamada apontado pela _lpfnFilterColumns_.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e das colunas especificadas foram movidas ou adicionadas.
    
## <a name="remarks"></a>Coment�rios

As propriedades passadas para **HrAddColumnsEx** usando o parâmetro _lpproptagColumnsNew_ se tornam as propriedades de primeira expostas nas chamadas para o método [IMAPITable:: QueryRows](imapitable-queryrows.md) subsequentes. Todas as propriedades anteriormente na tabela que não foram especificadas no parâmetro _lpproptagColumnsNew_ são expostas após todas as propriedades adicionadas e movidas. 
  
Se houver qualquer tabela propriedades indefinidas quando **QueryRows** é chamado, eles são retornados com o tipo de propriedade PT_NULL e o identificador de propriedade PROP_ID_NULL. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrAddColumnsEx** permite que o chamador fornecer uma função de retorno de chamada para filtrar as colunas que já foram na tabela, por exemplo converter cadeias de caracteres do tipo de propriedade PT_UNICODE PT_STRING8. **HrAddColumnsEx** passa um ponteiro para a coluna existente anteriormente definido como o parâmetro para a função de retorno de chamada. A função de retorno de chamada pode alterar os dados na matriz de marca de propriedade, mas não é possível adicionar novas marcas. 
  
 **HrAddColumnsEx** primeiro chama a função de retorno de chamada se um será fornecido, e em seguida, adiciona ou move das colunas especificadas e finalmente chama [IMAPITable::SetColumns](imapitable-setcolumns.md). 
  
Os parâmetros de entrada _lpAllocateBuffer_ e _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente. Os valores exatos dos ponteiros passados para **HrAddColumnsEx** dependem se o chamador é um aplicativo cliente ou um provedor de serviços. Um cliente passa ponteiros para as funções MAPI com os nomes especificados. Um provedor de serviços passa os ponteiros ele recebidas em sua chamada de inicialização ou recuperado chamando o método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPITable::QueryColumns](imapitable-querycolumns.md)

