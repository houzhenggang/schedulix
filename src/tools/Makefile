#
# Copyright (c) 2000-2013 "independIT Integrative Technologies GmbH"
# 
# schedulix Enterprise Job Scheduling System
# 
# independIT Integrative Technologies GmbH [http://www.independit.de]
# mailto:contact@independit.de
# 
# This file is part of schedulix
# 
# schedulix is is free software: 
# you can redistribute it and/or modify it under the terms of the 
# GNU Affero General Public License as published by the 
# Free Software Foundation, either version 3 of the License, 
# or (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU Affero General Public License for more details.
# 
# You should have received a copy of the GNU Affero General Public License
# along with this program. If not, see <http://www.gnu.org/licenses/>.

CLASSES = MiniParse.class Scanner.class \
	  set_variable.class get_variable.class set_state.class rerun.class submit.class set_warning.class auto_restart.class

SUBDIRS = .

all: generate subdirs $(CLASSES)

new: clean all

generate: Scanner.java MiniParse.java

subdirs: commonsubdirs

clean: commonclean
	rm -f Scanner.java* 
	rm -f MiniParse.java* 

include $(SDMSHOME)/src/Makefile.CommonRules

Scanner.java: Scanner.jlex
	$(JLEX) Scanner.jlex

MiniParse.java: MiniParse.jlex
	$(JLEX) MiniParse.jlex

