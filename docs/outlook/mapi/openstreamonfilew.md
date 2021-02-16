---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406021"
---
# <a name="openstreamonfilew"></a>OpenStreamOnFileW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aloca e inicializa um objeto OLE **IStream** para acessar o conteúdo de um arquivo. Essa função assume cadeias de caracteres UNICODE como argumentos, ao contrário da versão ANSI desta função [OpenStreamOnFile](openstreamonfile.md)e, portanto, permite caracteres arbitrários no nome do arquivo, incluindo o caminho e a extensão de arquivo.
  
|||
|:-----|:-----|
|Exportado por:  <br/> |olmapi32.dll  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parâmetros

 _lpAllocateBuffer_
  
> [in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores usados para controlar a criação ou abertura do arquivo a ser acessado por meio do objeto **IStream** OLE. Os sinalizadores a seguir podem ser definidos: 
    
SOF_UNIQUEFILENAME
  
> Um arquivo temporário deve ser criado para o **objeto IStream.** Se esse sinalizador estiver definido, os sinalizadores STGM_CREATE e STGM_READWRITE também deverão ser definidos. 
    
STGM_CREATE
  
> O arquivo deve ser criado mesmo que já exista um. Se o  _parâmetro lpszFileName_ não estiver definido, esse sinalizador e STGM_DELETEONRELEASE deverão ser definidos. Se STGM_CREATE estiver definido, o STGM_READWRITE também deverá ser definido. 
    
STGM_DELETEONRELEASE
  
> O arquivo deve ser excluído quando o **objeto IStream** for liberado. Se o  _parâmetro lpszFileName_ não estiver definido, esse sinalizador e STGM_CREATE deverão ser definidos. 
    
STGM_READ
  
> O arquivo deve ser criado ou aberto com acesso somente leitura.
    
STGM_READWRITE
  
> O arquivo deve ser criado ou aberto com permissão de leitura/gravação. Se esse sinalizador não estiver definido, o STGM_CREATE não deverá ser definido.
    
 _lpszFileName_
  
> [in] O nome do arquivo, incluindo caminho e extensão, do arquivo nomeado Unicode para o qual **OpenStreamOnFileW** inicializa o **objeto IStream.** Se o SOF_UNIQUEFILENAME sinalizador estiver definido,  _lpszFileName_ conterá o caminho para o diretório no qual será criado um arquivo temporário. Se  _lpszFileName_ for NULL, **OpenStreamOnFileW** obterá um caminho apropriado do sistema, e os sinalizadores STGM_CREATE e STGM_DELETEONRELEASE devem ser definidos. 
    
 _lpszPrefix_
  
> [in] O prefixo do nome de arquivo Unicode no qual **OpenStreamOnFileW** inicializa o **objeto IStream.** Se definido, o prefixo não deve conter mais de três caracteres. Se  _lpszPrefix_ for NULL, será usado um prefixo "SOF". 
    
 _lppStream_
  
> [out] Ponteiro para um ponteiro para um objeto expondo a interface **IStream.** 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_ACCESS
  
> O arquivo não pôde ser acessado devido a permissões de usuário insuficientes ou porque arquivos somente leitura não podem ser modificados.
    
MAPI_E_NOT_FOUND
  
> O arquivo designado não existe.
    
## <a name="remarks"></a>Comentários

A **função OpenStreamOnFileW** tem dois usos importantes, além de manipular um arquivo com um nome Unicode, diferenciado pela configuração do sinalizador SOF_UNIQUEFILENAME caracteres. Quando esse sinalizador não está definido, **OpenStreamOnFileW** abre um objeto **IStream** em um arquivo existente, por exemplo, para copiar seu conteúdo para a propriedade **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) de um anexo usando o método **IStream::CopyTo.** Nesse caso, o  _parâmetro lpszFileName_ especifica o caminho e o nome de arquivo do arquivo. 
  
Quando SOF_UNIQUEFILENAME é definido, **o OpenStreamOnFileW** cria um arquivo temporário para manter os dados de um **objeto IStream.** Para esse uso, o parâmetro  _lpszFileName_ pode, opcionalmente, designar o caminho para o diretório onde o arquivo deve ser criado, e o parâmetro  _lpszPrefix_ pode, opcionalmente, especificar um prefixo para o nome de arquivo. 
  
Quando o aplicativo cliente ou provedor de serviços de chamada for concluído com o objeto **IStream,** ele deverá liberá-lo chamando o método **OLE IStream::Release.** 
  
MAPI uses the functions pointed to  _by lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such [as IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O SOF_UNIQUEFILENAME sinalizador é usado para criar um arquivo temporário com um nome exclusivo para o sistema de mensagens. Se esse sinalizador estiver definido, o parâmetro  _lpszFileName_ especifica o caminho do arquivo temporário e o parâmetro  _lpszPrefix_ contém os caracteres de prefixo do nome do arquivo. O nome de arquivo construído é <prefix> HHHH. TMP, onde HHHH é um número hexadecimal. Se  _lpszFileName_ for NULL, o arquivo será criado no diretório de arquivos temporários retornado da função **Windows GetTempPath** ou no diretório atual se nenhum diretório de arquivos temporário tiver sido designado.
  
Se o sinalizador SOF_UNIQUEFILENAME não estiver definido,  _lpszPrefix_ será ignorado e  _lpszFileName_ deverá conter o caminho totalmente qualificado e o nome de arquivo do arquivo a ser aberto ou criado. O arquivo será aberto ou criado com base nos outros sinalizadores definidos em _ulFlags._
  
## <a name="see-also"></a>Confira também



[OpenStreamOnFile](openstreamonfile.md)

