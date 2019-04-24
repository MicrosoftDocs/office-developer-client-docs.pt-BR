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
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321711"
---
# <a name="imapiforminfosaveform"></a>IMAPIFormInfo::SaveForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Salva uma descrição de um formulário específico em um arquivo de configuração.
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a>Parâmetros

 _szFileName_
  
> no Uma cadeia de caracteres que nomeia o arquivo de mensagem de descrição do formulário, onde sua descrição é salva. Esse nome de arquivo deve ter a extensão. FDM.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_EXTENDED_ERROR 
  
> Não foi possível gravar o arquivo de configuração. Para obter a estrutura [MAPIERROR](mapierror.md) associada ao erro, chame o método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) . 
    
MAPI_E_NO_SUPPORT 
  
> **SaveForm** provavelmente foi chamado para salvar um formulário no contêiner de formulário local. Não há suporte para **SaveForm** no contêiner de formulários local. 
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormInfo:: SaveForm** para salvar uma descrição do formulário atual no arquivo com o nome de arquivo especificado. **SaveForm** cria um arquivo de configuração. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode reinstalar formulários selecionando-os em uma lista de mensagens do descritor de formulários em uma caixa de diálogo que os provedores de biblioteca de formulários exibem. A extensão recomendada para mensagens do descritor de formulários é. FDM.
  
Chame o método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) se **SaveForm** retornar MAPI_E_EXTENDED_ERROR e marque a estrutura de **MAPIERROR** retornada para determinar a condição que causou o erro. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[MAPIERROR](mapierror.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)

