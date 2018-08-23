---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 87f5e3f159542359f614a6ab698e6f06a2faf41a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567913"
---
# <a name="imapisupportregisterpreprocessor"></a>IMAPISupport::RegisterPreprocessor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra função pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ). 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMuid_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador que manipula a função pré-processador. O parâmetro _lpMuid_ pode ser NULL. 
    
 _lpszAdrType_
  
> [in] Um ponteiro para o tipo de endereço para as mensagens a função opera em, como X500, SMTP ou FAX. O parâmetro _lpszAdrType_ pode ser NULL. 
    
 _lpszDLLName_
  
> [in] Um ponteiro para o nome da biblioteca de vínculo dinâmico (DLL) que contém o ponto de entrada para a função de pré-processador.
    
 _lpszPreprocess_
  
> [in] Um ponteiro para o nome da função pré-processador. O parâmetro _lpszPreprocess_ pode ser NULL. 
    
 _lpszRemovePreprocessInfo_
  
> [in] Um ponteiro para o nome da função que removem informações pré-processador (uma função que está em conformidade com o protótipo [RemovePreprocessInfo](removepreprocessinfo.md) ). O parâmetro _lpszRemovePreprocessInfo_ pode ser NULL. 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A função pré-processador foi registrada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::RegisterPreprocessor** é implementado para transporte provedor suporte apenas os objetos. Provedores de transporte chamarem **RegisterPreprocessor** para registrar uma função pré-processador (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ). Uma função pré-processador deve ser registrada antes do MAPI spooler pode chamá-lo. 
  
Os parâmetros _lpszPreprocess_, _lpszRemovePreprocessInfo_e _lpszDLLName_ devem apontar para as cadeias de caracteres que podem ser usadas em conjunto com as chamadas para a função Win32 **GetProcAddress** , permitindo que DLL do pré-processador ponto de entrada a ser chamado corretamente. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chamadas para pré-processador são específicas a ordem do provedor de transporte. Isso significa que se outro provedor de transporte, além do seu provedor for capaz de lidar com uma mensagem, sua função pré-processador não será chamada para essa mensagem. Somente para mensagens que você irá lidar com sua função pré-processador será chamada.
  
Você pode escrever pré-processador funções para manipular um identificador específico armazenado em uma estrutura [MAPIUID](mapiuid.md) ou um tipo de endereço. Se você especificar ambas uma estrutura **MAPIUID** no parâmetro _lpMuid_ e um tipo de endereço no parâmetro _lpszAdrType_ , sua função será chamada para os destinatários da mensagem que correspondem a **MAPIUID** ou o tipo de endereço. Se _lpMuid_ é NULL e _lpszAdrType_ é não-nulo, sua função será chamada somente para os destinatários que tiverem um endereço que corresponde ao tipo apontado pela _lpszAdrType_. Se _lpMuid_ for não-nulos e _lpszAdrType_ é NULL, sua função será chamada para destinatários que correspondem a **MAPIUID**, independentemente de seu tipo de endereço. Se ambos forem NULL, sua função é chamada para todos os destinatários da mensagem.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[PreprocessMessage](preprocessmessage.md)
  
[RemovePreprocessInfo](removepreprocessinfo.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

