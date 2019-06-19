---
ms.openlocfilehash: 92b3aa8ebf6a4c0d6968287fd09d84d4415d47f5
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2019
ms.locfileid: "63872744"
---
> [!NOTE]
> <span data-ttu-id="9da75-101">**Linux および macOS システム上で実行されている .NET Core のみ:** C と Posix のカルチャの照合順序の動作では、大文字小文字が常に区別されます。これらのカルチャでは想定されている Unicode 照合順序が使われないためです。</span><span class="sxs-lookup"><span data-stu-id="9da75-101">**.NET Core running on Linux and macOS systems only:** The collation behavior for the C and Posix cultures is always case-sensitive because these cultures do not use the expected Unicode collation order.</span></span> <span data-ttu-id="9da75-102">カルチャに依存する、大文字と小文字を区別しない並べ替え操作を実行する場合は、C または Posix 以外のカルチャを使うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9da75-102">We recommend that you use a culture other than C or Posix for performing culture-sensitive, case-insensitive sorting operations.</span></span>  
