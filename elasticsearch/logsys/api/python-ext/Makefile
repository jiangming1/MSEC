
#
# Tencent is pleased to support the open source community by making MSEC available.
#
# Copyright (C) 2016 THL A29 Limited, a Tencent company. All rights reserved.
#
# Licensed under the GNU General Public License, Version 2.0 (the "License"); 
# you may not use this file except in compliance with the License. You may 
# obtain a copy of the License at
#
#     https://opensource.org/licenses/GPL-2.0
#
# Unless required by applicable law or agreed to in writing, software distributed under the 
# License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,
# either express or implied. See the License for the specific language governing permissions
# and limitations under the License.
#



LIB=log_py.so

PYINC=
PYLIB=-lpython2.7
LOGINC=../src
LOGLIB=-L../src -llogsys_api
CC=g++
SRC=$(wildcard *.cpp)
OBJ=$(SRC:.cpp=.o)
CFLAGS=-g -Wall -O2 -fPIC

all:$(LIB) 

$(LIB):$(SRC)
	$(CC) $(CFLAGS) $(SRC) -o $(LIB) -shared  -I$(LOGINC) $(LOGLIB) -I$(PYINC) $(PYLIB)
	install $(LIB) ../lib/

clean:
	-rm $(LIB)
