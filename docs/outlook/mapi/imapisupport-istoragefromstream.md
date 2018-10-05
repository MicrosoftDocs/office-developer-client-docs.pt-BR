---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392827"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementa um objeto de armazenamento para acessar um stream.
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parâmetros

 _lpUnkIn_
  
> [in] Um ponteiro para um objeto stream.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o fluxo apontado pela _lpUnkIn_. Qualquer um dos seguintes valores são válidos: IID_IStream, IID_ILockBytes, ou **Nulo**, que indica que a interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) deve ser usada para acessar o fluxo. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao objeto stream. Por padrão, o armazenamento é criado com acesso somente leitura e o fluxo começa na posição zero no armazenamento. Sinalizadores a seguir podem ser definidos:
    
STGSTRM_CREATE 
  
> Deve ser criado um novo objeto de armazenamento para o objeto stream.
    
STGSTRM_CURRENT 
  
> O objeto de armazenamento deve iniciar na posição atual do fluxo.
    
STGSTRM_MODIFY 
  
> O chamador deve ter permissão de leitura/gravação para o objeto de armazenamento retornado.
    
STGSTRM_RESET 
  
> O objeto de armazenamento deve iniciar na posição zero.
    
 _lppStorageOut_
  
> [out] Um ponteiro para um ponteiro para o objeto de armazenamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de armazenamento foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::IStorageFromStream** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços de chamarem **IStorageFromStream** para criar um objeto de armazenamento a ser usado para abrir propriedades específicas. Provedores de serviço que tem sua própria implementação da interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) não precisará chamar **IStorageFromStream**. 
  
O objeto de armazenamento criado pelo **IStorageFromStream** chama [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) método do fluxo para incrementar sua contagem de referência e diminui a contagem quando o armazenamento for lançado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de um dos seus objetos é chamado para abrir uma propriedade com a interface **IStorage** , execute as seguintes tarefas: 
  
1. Abra um objeto stream com permissão de leitura/gravação para a propriedade.
    
2. Marca internamente o fluxo de propriedade como um objeto de armazenamento.
    
3. Chame **IStorageFromStream** para gerar um objeto de armazenamento. 
    
4. Retorne um ponteiro para este objeto de armazenamento.
    
Se você implementar interfaces adicionais que usam o objeto de armazenamento, crie um objeto que envolve o objeto de armazenamento e implementar um método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de nível superior. 
  
Não permita a ser aberto com a interface **IStream** se ele foi criado com **IStorage**uma propriedade. Por outro lado, não permita uma propriedade a ser aberto com a interface **IStorage** se ele foi criado com **IStream**. 
  
Com uma exceção, ela é aceitável para usar a interface de **IStreamDocfile** para um objeto de armazenamento de um contêiner para outro stream, mas o identificador de interface IID_IStreamDocfile deve ser passado **OpenProperty** do método _lpInterface _parâmetro. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

