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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316583"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Implementa um objeto de armazenamento para acessar um fluxo.
  
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
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o fluxo apontado por  _lpUnkIn_. Qualquer um dos seguintes valores são válidos: IID_IStream, IID_ILockBytes ou **nulo**, o que indica que a interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) deve ser usada para acessar o fluxo. 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao objeto stream. Por padrão, o armazenamento é criado com acesso somente leitura e o fluxo começa na posição zero no armazenamento. Os sinalizadores a seguir podem ser definidos:
    
STGSTRM_CREATE 
  
> Um novo objeto de armazenamento deve ser criado para o objeto stream.
    
STGSTRM_CURRENT 
  
> O objeto de armazenamento deve iniciar na posição atual do fluxo.
    
STGSTRM_MODIFY 
  
> O chamador deve ter permissão de leitura/gravação para o objeto de armazenamento retornado.
    
STGSTRM_RESET 
  
> O objeto de armazenamento deve começar na posição zero.
    
 _lppStorageOut_
  
> [out] Um ponteiro para um ponteiro para o objeto de armazenamento.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de armazenamento foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::IStorageFromStream** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços **chamam IStorageFromStream para** criar um objeto de armazenamento a ser usado para abrir propriedades específicas. Os provedores de serviços que têm sua própria implementação da interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) não precisam chamar **IStorageFromStream**. 
  
O objeto de armazenamento criado por **IStorageFromStream** chama o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) do fluxo para incrementar sua contagem de referência e diminui a contagem quando o armazenamento é liberado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando o [método IMAPIProp::OpenProperty](imapiprop-openproperty.md) de um de seus objetos for chamado para abrir uma propriedade com a interface **IStorage,** execute as seguintes tarefas: 
  
1. Abra um objeto stream com permissão de leitura/gravação para a propriedade.
    
2. Marcar internamente o fluxo de propriedades como um objeto de armazenamento.
    
3. Chame **IStorageFromStream para** gerar um objeto de armazenamento. 
    
4. Retorne um ponteiro para esse objeto de armazenamento.
    
Se você implementar interfaces adicionais que usam o objeto de armazenamento, crie um objeto que envolva o objeto de armazenamento e implemente um método [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de nível superior. 
  
Não permita que uma propriedade seja aberta com a interface **IStream** se ela tiver sido criada com **IStorage**. Por outro lado, não permita que uma propriedade seja aberta com a interface **IStorage** se ela tiver sido criada com **IStream**. 
  
Com uma exceção, é aceitável usar a interface **IStreamDocfile** para transmitir um objeto de armazenamento de um contêiner para outro, mas o identificador da interface IID_IStreamDocfile deve ser passado no parâmetro _lpInterface_ do método **OpenProperty.** 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

