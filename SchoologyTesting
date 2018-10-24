import requests
import schoolopy
import yaml

with open('config.yml', 'r') as f:
	cfg = yaml.load(f)

sc = schoolopy.Schoology(schoolopy.Auth(cfg['key'], cfg['secret']))
sc.limit = 10 #10 obj max

print('School Information: %s' % sc.get_schools())
#print('School Buildings: %s' % sc.get_buildings(289049748))
print('Your name is %s' % sc.get_me().name_display)
#print('All users at Fairfield Prep: %s' % sc.get_users())
#print('Creating Building: %s' % sc.create_building(289049748, 'Xavier'))
print('Data on British Writers: %s' % sc.get_course(1673531420))
#print('Sections: %s' % sc.get_sections()) #it erred
#print('Section Enrollment: %s' % sc.get_section_enrollments(1673531420) 
print('British Writers, Upcoming Assignments: %s' % sc.get_assignments(1673531420))
#print('Brendans Recent Activity %s' % sc.get_user_actions(69821137))
keywords = Drama
print('Search Result for Drama: $s' % sc.search_courses(keywords))
for update in sc.get_feed():
	user = sc.get_user(update.uid)

#	print('By: ' + user.name_display)
#	print(update.body[:40].replace('\r\n', ' ').replace('/n', ' ') + '...')
#	print('%d likes/n' % update.likes)
