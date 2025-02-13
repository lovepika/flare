# Copyright (C) 2021 THL A29 Limited, a Tencent company. All rights reserved.
#
# Licensed under the BSD 3-Clause License (the "License"); you may not use this
# file except in compliance with the License. You may obtain a copy of the
# License at
#
# https://opensource.org/licenses/BSD-3-Clause
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
# WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
# License for the specific language governing permissions and limitations under
# the License.

cc_library(
  name = 'native',
  hdrs = [
    'acceptor.h',
    'datagram_transceiver.h',
    'stream_connection.h',
  ],
  srcs = [
    'acceptor.cc',
    'datagram_transceiver.cc',
    'stream_connection.cc',
  ],
  deps = [
    '//flare/base:align',
    '//flare/base:buffer',
    '//flare/base:exposed_var',
    '//flare/base:function',
    '//flare/base:likely',
    '//flare/base:logging',
    '//flare/base:maybe_owning',
    '//flare/base:object_pool',
    '//flare/base/net:endpoint',
    '//flare/fiber:alternatives',
    '//flare/io:acceptor',
    '//flare/io:datagram_transceiver',
    '//flare/io:io_basic',
    '//flare/io:stream_connection',
    '//flare/io/detail:eintr_safe',
    '//flare/io/detail:read_at_most',
    '//flare/io/detail:writing_buffer_list',
    '//flare/io/detail:writing_datagram_list',
    '//flare/io/util:rate_limiter',
    '//flare/io/util:socket',
    '//flare/io/util:stream_io',
  ],
  visibility = 'PUBLIC',
)

cc_test(
  name = 'acceptor_test',
  srcs = 'acceptor_test.cc',
  deps = [
    ':native',
    '//flare/io:io_basic',
    '//flare/io/util:socket',
    '//flare/testing:endpoint',
    '//flare/testing:main',
  ]
)

cc_test(
  name = 'stream_connection_test',
  srcs = 'stream_connection_test.cc',
  deps = [
    ':native',
    '//flare/base:string',
    '//flare/fiber:fiber',
    '//flare/io:io_basic',
    '//flare/io/util:socket',
    '//flare/testing:endpoint',
    '//flare/testing:main',
  ]
)

cc_test(
  name = 'datagram_transceiver_test',
  srcs = 'datagram_transceiver_test.cc',
  deps = [
    ':native',
    '//flare/io:io_basic',
    '//flare/io/util:socket',
    '//flare/testing:endpoint',
    '//flare/testing:main',
  ]
)
