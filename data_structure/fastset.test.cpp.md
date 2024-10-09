---
data:
  _extendedDependsOn: []
  _extendedRequiredBy: []
  _extendedVerifiedWith: []
  _isVerificationFailed: true
  _pathExtension: cpp
  _verificationStatusIcon: ':x:'
  attributes: {}
  bundledCode: "Traceback (most recent call last):\n  File \"/opt/hostedtoolcache/Python/3.12.7/x64/lib/python3.12/site-packages/onlinejudge_verify/documentation/build.py\"\
    , line 71, in _render_source_code_stat\n    bundled_code = language.bundle(stat.path,\
    \ basedir=basedir, options={'include_paths': [basedir]}).decode()\n          \
    \         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^\n\
    \  File \"/opt/hostedtoolcache/Python/3.12.7/x64/lib/python3.12/site-packages/onlinejudge_verify/languages/cplusplus.py\"\
    , line 187, in bundle\n    bundler.update(path)\n  File \"/opt/hostedtoolcache/Python/3.12.7/x64/lib/python3.12/site-packages/onlinejudge_verify/languages/cplusplus_bundle.py\"\
    , line 401, in update\n    self.update(self._resolve(pathlib.Path(included), included_from=path))\n\
    \                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^\n \
    \ File \"/opt/hostedtoolcache/Python/3.12.7/x64/lib/python3.12/site-packages/onlinejudge_verify/languages/cplusplus_bundle.py\"\
    , line 260, in _resolve\n    raise BundleErrorAt(path, -1, \"no such header\"\
    )\nonlinejudge_verify.languages.cplusplus_bundle.BundleErrorAt: FastSet.hpp: line\
    \ -1: no such header\n"
  code: "#define PROBLEM \"https://judge.yosupo.jp/problem/predecessor_problem\"\n\
    #include \"FastSet.hpp\"\n#include <bits/stdc++.h>\nusing namespace std;\n\nint\
    \ main() {\n   cin.tie(0)->sync_with_stdio(0);\n   int N, Q;\n   cin >> N >> Q;\n\
    \   string S;\n   cin >> S;\n   FastSet s(N);\n   for(int i = 0; i < N; i++) if(S[i]\
    \ == '1') s.set(i);\n   while(Q--) {\n      int c, k;\n      cin >> c >> k;\n\
    \      if(c == 0) s.set(k);\n      if(c == 1) s.reset(k);\n      if(c == 2) cout\
    \ << (s.a[0][k / FastSet::B] >> (k % FastSet::B) & 1) << '\\n';\n      if(c ==\
    \ 3) {\n         int ans = s.next(k - 1);\n         cout << (ans == N ? -1 : ans)\
    \ << '\\n';\n      }\n      if(c == 4) cout << (int)s.prev(k + 1) << '\\n';\n\
    \   }\n}"
  dependsOn: []
  isVerificationFile: true
  path: data_structure/fastset.test.cpp
  requiredBy: []
  timestamp: '1970-01-01 00:00:00+00:00'
  verificationStatus: TEST_WRONG_ANSWER
  verifiedWith: []
documentation_of: data_structure/fastset.test.cpp
layout: document
redirect_from:
- /verify/data_structure/fastset.test.cpp
- /verify/data_structure/fastset.test.cpp.html
title: data_structure/fastset.test.cpp
---
