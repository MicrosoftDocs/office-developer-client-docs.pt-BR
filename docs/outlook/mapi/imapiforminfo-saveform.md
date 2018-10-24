---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7fec6b6236d26789a3ec9abee7d2ae1c620f89b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593470"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Salva uma descrição de um determinado formulário em um arquivo de configuração.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parâmetros

 _szFileName_
  
> [in] Uma cadeia de caracteres que nomeia o arquivo de mensagem de descrição do formulário onde a respectiva descrição é salva. Este nome de arquivo deve ter a extensão .fdm.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_EXTENDED_ERROR 
  
> Não foi possível gravar o arquivo de configuração. Para obter a estrutura [MAPIERROR](mapierror.md) que está associada com o erro, chame o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** provavelmente foi chamado para salvar um formulário no contêiner local do formulário. **SaveForm** não é suportado no contêiner do local do formulário. 
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método de **IMAPIFormInfo::SaveForm** para salvar uma descrição do formulário atual no arquivo que tenha o nome de arquivo fornecido. **SaveForm** cria um arquivo de configuração. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode reinstalar formulários selecionando-os em uma lista de mensagens descritor de formulário em uma caixa de diálogo que compõem a exibição de provedores de biblioteca. A extensão recomendada para mensagens de descritor de formulário é .fdm.
  
Chamar o método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) se **SaveForm** retorna MAPI_E_EXTENDED_ERROR e verificar a estrutura **MAPIERROR** retornada para determinar a condição que causou o erro. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

